# ⚙️ Batch Job – Inventory Refill Automation

This batch job automatically updates inventory for products with low stock levels.

---

## 🧠 Purpose

- Run daily to check which products have `Stock_Quantity__c < 10`
- Add 50 units to each such product
- Scheduled to run every night at 12:00 AM

---

🕒 Schedule via Anonymous Execution
To schedule the batch job daily at midnight:

Go to Developer Console → Debug → Open Execute Anonymous Window

Paste and run the following code:

System.schedule('Daily Inventory Sync', '0 0 0 * * ?', new InventoryBatchJob());

<img width="1852" height="821" alt="Screenshot 2025-07-13 004526" src="https://github.com/user-attachments/assets/60f02457-4fbb-4ad3-bdc1-4fcf4f90df0f" />
<img width="1562" height="685" alt="Screenshot 2025-07-13 004608" src="https://github.com/user-attachments/assets/a323569d-a64b-4869-bf2f-fa71cbd546ba" />
