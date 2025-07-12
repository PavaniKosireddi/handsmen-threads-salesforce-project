# ✅ Validation Rules – HandsMen Threads

This document outlines the key validation rules implemented to maintain data integrity across custom objects in the Salesforce HandsMen Threads project.

---

## 1️⃣ HandsMen Order

**Object:** `HandsMen_Order__c`  
**Field:** `Total_Amount__c`  
**Purpose:** Prevent saving orders with total amount less than or equal to zero.

**Validation Rule:**

Total_Amount__c <= 0
<img width="1896" height="369" alt="Screenshot 2025-07-12 224234" src="https://github.com/user-attachments/assets/f309006f-0480-4005-97f0-aec4c25e1bb5" />


2️⃣ Inventory
Object: Inventory__c
Field: Stock_Quantity__c
Purpose: Prevent saving inventory records with zero or negative stock values.

Validation Rule:
Stock_Quantity__c <= 0

<img width="1914" height="417" alt="Screenshot 2025-07-12 224251" src="https://github.com/user-attachments/assets/bba33e32-d9c1-4a33-a6d2-c5a58c8a99dc" />

3️⃣ HandsMen Customer
Object: HandsMen_Customer__c
Field: Email
Purpose: Ensure that only Gmail addresses are allowed for customer emails.

Validation Rule:
NOT CONTAINS(Email, "@gmail.com")

<img width="1903" height="438" alt="Screenshot 2025-07-12 224307" src="https://github.com/user-attachments/assets/8ddf4d7a-4862-4c4a-b8d8-a22599e6ec55" />

