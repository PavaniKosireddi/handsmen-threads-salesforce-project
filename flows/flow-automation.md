# 🔁 Automation Flows – HandsMen Threads

This file documents the three automation flows configured to enhance operations in the HandsMen Threads Salesforce org.

---

## 📧 1️⃣ Order Confirmation Flow (Record-Triggered)

**Trigger Object**: `HandsMen_Order__c`  
**Trigger Condition**: When a record is updated AND `Status__c` = "Confirmed"  
**Frequency**: Only when a record is updated to meet the condition  
**Action**: Send email alert to customer

### 📌 Flow Steps:
- Record-Triggered Flow → Object: `HandsMen_Order__c`
- Triggered when `Status__c` becomes `"Confirmed"`
- Action → Send Email Alert → Template: *Order Confirmation Email*
- Label: `Send Order Confirmation Email`
- Record ID: `{$Record.Id}`
<img width="465" height="494" alt="Screenshot 2025-07-13 002535" src="https://github.com/user-attachments/assets/9ed2aeec-7d11-432f-a73e-3c40faf07727" />


## 🚨 2️⃣ Stock Alert Flow (Record-Triggered)

**Trigger Object**: `Inventory__c`  
**Trigger Condition**: When a record is created or updated AND `Stock_Quantity__c < 5`  
**Frequency**: Every time a record is created/updated and meets the condition  
**Action**: Send email alert to warehouse manager

### 📌 Flow Steps:
- Record-Triggered Flow → Object: `Inventory__c`
- Trigger: Created/Updated → Condition: `Stock_Quantity__c < 5`
- Action → Send Email Alert → Recipient: Inventory Manager
- Email Alert: *Stock Alert Email Template*
<img width="442" height="466" alt="Screenshot 2025-07-13 002529" src="https://github.com/user-attachments/assets/857fd3b9-1bb1-4058-ac29-32edeff88029" />

---

## 🕒 3️⃣ Loyalty Status Update Flow (Scheduled Flow)

**Trigger**: Scheduled – Daily  
**Object**: `HandsMen_Customer__c`  
**Purpose**: Update `Loyalty_Status__c` daily based on `Total_Purchases__c`

### 🧠 Logic:
| Condition | Loyalty_Status__c |
|-----------|-------------------|
| `> 1000`  | `Gold`            |
| `< 500`   | `Bronze`          |
| Else      | `Silver`          |

### 📌 Flow Structure:
1. **Get Records** → All customers
2. **Loop** → Through each customer
3. **Decision** →
    - `> 1000` → Gold
    - `< 500` → Bronze
    - Else → Silver
4. **Update Records** → Set appropriate `Loyalty_Status__c` per branch
<img width="1367" height="638" alt="Screenshot 2025-07-13 002518" src="https://github.com/user-attachments/assets/765e7a4d-794c-4f73-82e0-a156813bfb7b" />


