 foxpro-vm-setup
# **Setting up Windows XP VM on WMWare Workstation Pro for Visual FoxPro Programming**


**Overview**: This is a full guide that walks you through creating a safe and secure virtual machine (VM) running Windows XP, for Visual FoxPro programming. It is served for learners and developers who want a risk-free environment for legacy development.

### **Step 1: Tools to Prepare**
Required Software:
* VMWare Workstation Pro
* Windows XP Professional 32-bit ISO (e.g. from archive.org)
* Valid XP Product Key (e.g from old PC COA sticker)
* Visual FoxPro Installer (version 6.0 to 9.0)

### **Step 2: Setting Up a Virtual Machine**
1. Open VMWare Workstation Pro and click **Create a New Virtual Machine**.
2. Choose **Typical (recommended)**, then click Next.
3. Choose **Installer disc image file (iso)**: and browse to your Windows XP ISO file.
4. Click **Next**, then enter your Windows XP product key and set a username.
5. Name your VM (e.g., "Windows XP FoxPro") and choose a storage location.
6. Set the minimum disk size to 10-20 GB and select **Store virtual disk as a single file**.
7. Customize your hardware:
   * Set at least **512 MB RAM** (1 GB recommended)
   * Go to **CD/DVD (IDE)** and confirm the XP ISO is mounted.
   * Go to **Hard Disk** and check if it uses **SATA**,            change it to IDE (prevents detection issues during            installation).
8. Click **Finish** to create the VM.

### **Step 3: Boot and Install Windows XP**

1. Power off the VM.
2. The VM will boot from the ISO and start the Windows XP installation.
3. If you encounter "Setup did not find any hard disk drives installed":
   * Power off the VM.
   * Edit VM settings > **Hard Disk**  > Change type to IDE        if needed.

4. Complete the XP installaton by following the setup prompts.
5. Enter the product key if not pre-filled, and finish installation.

### **Step 4: Keep the Virtual Machine Secure**

1. After installing XP:
   * Refer to **VM > Settings > Network Adapter**.
   * Change to **Host-only** to prevent internet access yet        allowing file sharing.
2. (Optional) Enable **Shared Folders**:
   * Go to **VM > Settings > Options > Shared Folders**.
   * Enable and add a shared folder to transfer files between      your host and XP VM.
3. Make sure to create a snapshot after setup to preserve a clean restore point.

### **Step 5: Install Visual FoxPro**

### **Option 1: Mount ISO Using VMWare**
1. Go to **VM > Settings > CD/DVD (IDE)**.
2. Choose **Use ISO image file**, browse and select your Visual FoxPro installer ISO.
3. The ISO will be mounted as a CD/DVD in the VM.

### **Option 2: Use Virtual CloneDrive to Mount ISO**
1. Inside the XP VM, install **Virtual CloneDrive**.
2. After install, right-click the ISO file of Visual FoxPro Installer and choose **Mount with Virtual CloneDrive**.
3. Open **My Computer**, access the new CD/DVD drive, and run _setup.exe_

### **Complete the Installation**
1. Follow the Visual FoxPro installation wizard.
2. Choose **Full** or **Custom** install.
3. After install, verify it works:
   * Open Visual FoxPro
   * Run a test line: `? "Hello World"`

### **Step 6: Keeping Your Environment Safe**
* Keep your VM in **Host-only** mode for safety.
* Use **Shared Folders** or **USB pass-through** to transfer code and files.
* Back up your FoxPro projects regularly.
* Take a **snapshot** after installation and major changes.


**Conclusion:** Using this guide, you may now have a fully functional and secure Windows XP virtual machine in VMWare Workstation Pro, fit for Visual FoxPro development. The setup mentioned above allows you to work with legacy software without the risk of affecting your host environment from the vulnerabilities of an outdated operating system. 

PS: This documentation is subject to change. I'm currently working on improving my documentation skills, so I apologize in advance for any inconsistencies. Thank you!


