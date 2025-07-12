# 🔐 Permission Set – HandsMen Threads

This document describes the configuration of the custom permission set used to grant object-level access to users with restricted profiles.

---

## 📛 Permission Set: Permission_Platform_1

### ✅ Purpose:
To grant full access (read, create, edit, delete) to key custom objects required by Platform 1 users (e.g., `Niklaus`).

---

## 📘 Object Permissions Granted

| Object                | Read | Create | Edit | Delete |
|-----------------------|------|--------|------|--------|
| HandsMen Customer     | ✅   | ✅     | ✅   | ✅     |
| HandsMen Order        | ✅   | ✅     | ✅   | ✅     |

> ⚠️ **Note:** Standard objects like `Order` were excluded due to the `Salesforce Platform` license limitation.

---

## 👥 Assigned To

| Username | Profile     | Role   |
|----------|-------------|--------|
| Niklaus  | Platform 1  | Sales  |

---


📌 **Permission Set Overview**  
<img width="1488" height="754" alt="Screenshot 2025-07-12 233137" src="https://github.com/user-attachments/assets/1a9ca8b3-8588-480c-b41e-eba55091b0f6" />


📌 **Customer Object Permissions**  
<img width="688" height="612" alt="Screenshot 2025-07-12 233239" src="https://github.com/user-attachments/assets/59e8cbd8-e74c-4395-aaaa-3aa9e2355b0c" />


📌 **Order Object Permissions**  
<img width="746" height="729" alt="Screenshot 2025-07-12 233257" src="https://github.com/user-attachments/assets/5a016d99-ac43-4d55-bdac-cc335f6cc03e" />

📌 **Assignment to User (Niklaus)**  
<img width="1834" height="446" alt="Screenshot 2025-07-12 233118" src="https://github.com/user-attachments/assets/f6cca8a5-8adf-4229-945c-4c8660a97941" />


---

## ✅ Summary

- Permission set successfully created and assigned
- Users can fully interact with necessary custom objects
- Validated under the `Salesforce Platform` license without errors
