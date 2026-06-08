# How to Access and Edit MT882 Router System Files

First of all, you have got to have the **Telnet Feature** enabled on Windows 10 or Windows 11.

##  How to Enable Telnet Client
1. Press `Windows + R` on your keyboard.
2. Type the following command and press Enter:
   ```text
   optionalfeatures
   ```
4. Scroll down, check the box for **Telnet Client**, and click **OK**.

---

##  Router Ethernet Cable Setup
1. Connect an Ethernet cable to your Laptop/PC.
2. Connect the other end to the back of the router into the port named **Ethernet**.
3. A light called **LAN** or **WAN** on the router should turn on.
4. Press `Windows + R` again and type:
   ```text
   ncpa.cpl
   ```
5. Double-click on **Ethernet**.
6. Click on **Properties**.
7. Double-click on **Internet Protocol Version 4 (TCP/IPv4)**.

---

##  IP Address Setup
1. Click on **Use the following IP address**.
2. Enter these exact values into the boxes:
   * **IP address:** `192.168.1.10` *(Note: This does not have to be your main home Wi-Fi/Ethernet IP)*
   * **Subnet mask:** `255.255.255.0`
   * **Default gateway:** `192.168.1.1`
3. Click **OK**, and then click **OK** again to finish setting up the IPs.

---

##  Editing System Files Via Telnet
1. Press `Windows + R` and type `cmd` to open the Command Prompt.
2. Inside the Command Prompt, connect to the gateway IP by typing:
   ```cmd
   telnet 192.168.1.1
   ```
3. It will ask you for a password. The default password is `admin`.
   * *If `admin` doesn't work, get a small paperclip or needle, press the physical **Reset** button on the back of the router, and try `admin` again.*
4. Once you are successfully logged in, the console prompt will change to look exactly like this:
   ```text
   MT882>
   ```
5. This is the main console of the MT882 Router. To modify the system files, type this command:
   ```text
   sys edit autoexec.net
   ```
6. Immediately after pressing **Enter**, press the `i` key as quickly as possible. 

**BOOM!** You can now edit the system files. 

> [!NOTE]
> This allows you to enable debug features or configure it as a firewall for another router (like an ASUS). You cannot edit the bootloader, main system OS, or firmware through this method.

---

## ⚠️ Safety Status
This process is **completely safe**. There is no risk of bricking your router or turning it into a useless brick. 

*I am currently trying to figure out how to edit the bootloader so you can flash custom firmware. Stay tuned!*
