# Windows_11_24H2_Network_Fix


 Windows 11 24H2 Network Issue Alert 🚨  

Some users have reported losing network connectivity (LAN & WLAN) after upgrading to **Windows 11 24H2**. This issue is caused by a missing gateway entry due to a **DHCP bug**. Even manually setting the gateway won’t work, as it resets after a restart.  

---

## 🛠️ Fix for Windows 11 Wi-Fi & DHCP Issue  

This is a **Windows bug**, **not a problem with your modem or router**. Follow these steps to restore your internet connection:  

### **Step 1: Open the Registry Editor** 🔍  
📌 Press **Win + R**, type **regedit**, and hit **Enter**.  

![Registry Editor](https://www.howtogeek.com/wp-content/uploads/2021/08/windows-11-registry-editor.png)  

---

### **Step 2: Navigate to the Registry Path** 📂  
📌 Go to:  

HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\WcmSvc



![Registry Path](https://www.winhelponline.com/blog/wp-content/uploads/2020/06/wifi-dhcp-bug-regedit.png)  

---

### **Step 3: Modify the DependOnService Entry** ✏️  
📌 Find **"DependOnService"**, double-click it, and **remove** the line:  

WinHTTPAutoProxySvc

✅ Click **OK** to save the changes.  

![Editing Registry](https://i.imgur.com/9s2xCGQ.png)  

---

### **Step 4: Restart Network Services** 🔄  
1️⃣ **Open Task Manager** (`Ctrl + Shift + Esc`).  
2️⃣ Go to the **Services** tab.  
3️⃣ Restart the following services:  
   - **Windows Connection Manager (WcmSvc)**  
   - **WLAN AutoConfig (WlanSvc)**  



![Task Manager Services](https://www.digitalcitizen.life/wp-content/uploads/2023/07/task_manager_services.png)  

---

✅ **This should restore your internet connection.**  

💬 **Spread the word** and let others know if this fix works for you!  
