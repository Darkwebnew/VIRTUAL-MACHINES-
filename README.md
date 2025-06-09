# EX - 6 MOVING FILES BETWEEN VIRTUAL MACHINES

## 🎯 AIM:
To move files between virtual machines (VMs) efficiently.

---

## 📘 Introduction:
You can move files between virtual machines using several methods:
- Using network utilities as on physical systems.
- Through host-only, bridged, or NAT networking modes.
- Using shared drives (virtual disks or raw partitions).
- Sharing a specific folder between host and guest OS using VirtualBox.

---

## 🛠️ PROCEDURE:

### ✅ Step 1: Install Guest Additions on the Guest Machine
1. Start the VirtualBox Guest Machine (OS).
2. From the VirtualBox top menu, go to:  
   `Devices > Insert Guest Additions CD image…`

   - a. Open **Windows Explorer**  
   - b. Double-click **CD Drive (X:) VirtualBox Guest Additions** to view contents.  
     ![image](https://github.com/user-attachments/assets/d3dbb341-38c1-4f3e-92f7-0cfe1084e679)

   - c. Right-click **VBoxWindowsAdditions** and choose **Run as Administrator**  
     ![image](https://github.com/user-attachments/assets/35be1b73-df5c-445e-bb24-94d71f7898e4)

3. Click **Next**, follow the on-screen instructions to install Guest Additions  
   ![image](https://github.com/user-attachments/assets/066c93ef-f2fa-40e8-a8f2-041ca2758db1)

4. After installation, click **Finish** and restart the guest machine.

---

### ✅ Step 2: Setup File Sharing on VirtualBox Guest Machine

1. From VirtualBox menu: `Devices > Shared Folders > Shared Folder Settings`  
   ![image](https://github.com/user-attachments/assets/c58d8e37-8a75-47ad-bdc8-800ff55b2ccf)

2. Click the **Add new shared folder** icon  
   ![image](https://github.com/user-attachments/assets/b7cb3277-4fce-4267-8916-04f94a41a2f8)

3. Click the drop-down arrow and select **Other**  
   ![image](https://github.com/user-attachments/assets/50268dcf-8b14-4592-9a69-439b0639db43)

4. From the Host OS, locate and select the folder to share.  
   > 💡 *Tip: Create a folder like "Public" on the Host for easy sharing.*  
   ![image](https://github.com/user-attachments/assets/076d8f8f-93cc-478e-902b-8d3d0b1474e6)

5. In **Add Share** options:  
   - Type a name (optional)  
   - Check `Auto-mount`  
   - Check `Make Permanent`  
   - Click **OK** twice  
   ![image](https://github.com/user-attachments/assets/3f2c7dc1-5781-43e3-8e36-4e0706d603e0)

6. Done! Open **Windows Explorer** in Guest OS.  
   - You’ll now see a new network drive under **Network Locations** that maps to your shared folder.

---

## ✅ RESULT:
Thus, file sharing between virtual machines has been successfully configured using VirtualBox Guest Additions and Shared Folder setup.
