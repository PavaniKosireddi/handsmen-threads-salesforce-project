# ⚙️ Apex Class & Trigger – Order Quantity Validation

This document explains the logic and implementation of an Apex class + trigger to maintain quantity validations for different order statuses.

---

## ✅ Apex Class: `OrderTriggerHandler`

This class contains reusable validation logic for:

| Order Status | Quantity Condition        |
|--------------|---------------------------|
| Confirmed    | Must be > 500             |
| Pending      | Must be > 200             |
| Rejection    | Must be exactly 0         |

📌 This logic is enforced before insert or update.

### Code:

```java
public class OrderTriggerHandler {
    public static void validateOrderQuantity(List<HandsMen_Order__c> orderList) {
        for (HandsMen_Order__c order : orderList) {
            if (order.Status__c == 'Confirmed') {
                if (order.Quantity__c == null || order.Quantity__c <= 500) {
                    order.Quantity__c.addError('For Status "Confirmed", Quantity must be more than 500.');
                }
            } else if (order.Status__c == 'Pending') {
                if (order.Quantity__c == null || order.Quantity__c <= 200) {
                    order.Quantity__c.addError('For Status "Pending", Quantity must be more than 200.');
                }
            } else if (order.Status__c == 'Rejection') {
                if (order.Quantity__c == null || order.Quantity__c != 0) {
                    order.Quantity__c.addError('For Status "Rejection", Quantity must be 0.');
                }
            }
        }
    }
}

<img width="1773" height="887" alt="Screenshot 2025-07-13 003404" src="https://github.com/user-attachments/assets/47a9705a-9df4-44fc-8309-5e2efbe7f2b8" />



## ✅ Apex Trigger: `OrderTrigger`

trigger OrderTrigger on HandsMen_Order__c (before insert, before update) {
    if (Trigger.isBefore && (Trigger.isInsert || Trigger.isUpdate)) {
        OrderTriggerHandler.validateOrderQuantity(Trigger.new);
    }
}
<img width="1187" height="403" alt="Screenshot 2025-07-13 003416" src="https://github.com/user-attachments/assets/29ca36a2-ea54-4512-b528-94d03e088fec" />

