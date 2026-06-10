# How to Access and Edit Huawei MT882 Router System Files

First of all, you have got to have the Telnet Feature On Windows 10/11.

## Wondering how to Enable it?
Press Windows + R, then type this command and press Enter:
```text
optionalfeatures
```
Select Telnet Client and click OK.

## Router Ethernet Cable Setup
Connect an Ethernet cable to your Laptop/PC, then connect it to the back of the router, the port named Ethernet. Then a light called LAN or WAN on the Router should turn on. After that, press again Windows + R and type this command:
```text
ncpa.cpl
```
Then double-click on Ethernet. After that, press properties and double-click on the Internet Protocol Version 4 (TCP/IPv4).

## Ip adress setup
After all that, press on "Use the following IP address". At the IP address box put `192.168.1.10` (it does not have to be your main Home Wifi/Ethernet IP). At Subnet Mask put the IP `255.255.255.0`. And finally, at the Default Gateway put `192.168.1.1`. Then click OK and OK again to finish setting up the IP's.

## Editing System Files Via Telnet
After all that, press Windows + R and type `cmd`. Then inside the Command Prompt type:
```text
telnet 192.168.1.1
```
(It's the Gateway IP that we set up earlier). And it should ask you for a password. The password should be `admin`. If not, get a small paperclip or needle or something thin and press the reset button (it should be on the back). After that, the password should be `admin`. 

If you got in the console, it should show:
```text
MT882>
```
That's the main console of the Huawei MT882 Router to modify the system files. Type:
```text
sys edit autoexec.net
```
And after pressing enter, press `i` as quickly as possible and BOOM! You can edit the system files now (except the bootloader or main system OS or firmware). You can only enable debug features and you can make it as a firewall for another router, ASUS etc.

## ⚠️ Safety Status
Completely safe, no bricking, no making the router a useless thing. I'll try to figure out how to edit the bootloader so you can flash custom firmware.
