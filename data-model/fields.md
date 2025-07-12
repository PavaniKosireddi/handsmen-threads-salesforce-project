# 🧩 Custom Object Fields – HandsMen Threads

This document outlines all key fields created under each custom object in Salesforce for the HandsMen Threads project.

---

## 👤 HandsMen Customer

| Field Label | Type | Notes |
|-------------|------|-------|
| Email | Email | – |
| Phone | Phone | – |
| Loyalty_Status__c | Picklist | Bronze, Silver, Gold |
| Total_Purchases__c | Number | – |

<img width="1854" height="846" alt="Screenshot 2025-07-12 222031" src="https://github.com/user-attachments/assets/50444e81-3de9-4827-aef7-b1aff66969b7" />

---

## 📦 HandsMen Product

| Field Label | Type |
|-------------|------|
| SKU | Text |
| Price | Currency |
| Stock_Quantity__c | Number |


---<img width="1916" height="732" alt="Screenshot 2025-07-12 222102" src="https://github.com/user-attachments/assets/400f1baf-2f02-4234-905e-1e319fd550b1" />


## 📄 HandsMen Order

| Field Label | Type |
|-------------|------|
| Order_Number (Record Name) | Text |
| Status | Picklist |
| Quantity__c | Number |
| Total_Amount__c | Number |

<img width="1898" height="748" alt="Screenshot 2025-07-12 222123" src="https://github.com/user-attachments/assets/d2477444-2240-479a-b67e-968e54ffe929" />

---

## 🏬 Inventory

| Field Label | Type |
|-------------|------|
| Auto Number (Record Name) | Auto Number |
| Warehouse | Text |
| Stock_Quantity__c | Number |


---<img width="1911" height="736" alt="Screenshot 2025-07-12 222142" src="https://github.com/user-attachments/assets/d573f8be-92a0-49ea-8b86-b08bfdb8578c" />


## 📢 Marketing Campaign

| Field Label | Type |
|-------------|------|
| Campaign_Name (Record Name) | Text |
| Start_Date | Date |
| End_Date | Date |

<img width="1911" height="750" alt="Screenshot 2025-07-12 222159" src="https://github.com/user-attachments/assets/d01cf83b-85f9-494f-8200-37603dd0b963" />
