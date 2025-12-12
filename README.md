# Home-Cyber-Lab-IT-Troubleshooting
This home lab uses Windows 10 and Ubuntu 24.04 to practice IT troubleshooting, system diagnostics, and basic network analysis. It includes VM setup, DNS troubleshooting, ICMP testing, and full documentation. I built a small IT lab in VirtualBox to learn and practice real entry-level troubleshooting tasks. The project helped me get comfortable with basic troubleshooting, networking commands, and system diagnostics across both Windows and Linux.

---

## Environment Setup

I did the following

* Installed a Windows 10 virtual machine  
* Installed an Ubuntu 24.04 LTS virtual machine  
* Set up VirtualBox networking so both VMs could reach the internet  
* Checked system details on Ubuntu with Linux commands

---

## Network And System Diagnostics

Commands I used on Ubuntu

* `hostnamectl`  show hostname and basic system info  
* `ip a`  view network interfaces and IP addresses  
* `ping 8.8.8.8`  test raw internet connectivity with ICMP  
* `ping google.com`  noticed DNS name resolution was not working at first  
* `nslookup google.com 1.1.1.9`  forced DNS query that failed and confirmed a DNS problem  
* `cat /etc/resolv.conf`  checked the current DNS resolver settings  
* Edited `/etc/resolv.conf`  pointed DNS to 1.1.1.1 and 8.8.8.8  
* `nslookup google.com`  tested DNS again after the fix  
* `sudo apt update`  confirmed package servers were reachable after DNS was fixed  
* `ping google.com`  final end to end test with a domain name

On Windows 10 I also

* Ran `ipconfig`  viewed adapter settings and default gateway  
* Ran `ping google.com`  confirmed DNS and connectivity from the Windows side

---

## Troubleshooting Work

I walked through these steps

* Saw that ping to 8.8.8.8 worked but ping to google.com failed at first  
* Used nslookup and resolv.conf to confirm it was a DNS resolver issue  
* Changed the Ubuntu DNS servers to 1.1.1.1 and 8.8.8.8  
* Retested with nslookup, ping, and sudo apt update until everything passed  
* Captured each step with screenshots so the full process is documented

---

## Screenshots

Screenshots used for this lab

1. `01_UbuntuDesktop.png`  Ubuntu desktop after boot  
2. `02_UbuntuhHostnamectl.png`  hostnamectl system info  
3. `03_UbuntuhuiIPAl.png`  ip a output with IP details  
4. `04_U_ping_test_.png`  ping 8.8.8.8 connectivity test  
5. `05_sudo_apt_update.png`  apt update before the DNS fix  
6. `06_googlelookip.png`  nslookup google.com  
7. `07_dns_fail.png`  nslookup google.com 1.1.1.9 showing DNS failure  
8. `08_resolv_conf_before_fix.png`  original resolv.conf settings before changes  
9. `08_resolv_conf_after_fix.png`  resolv.conf after pointing DNS to 1.1.1.1 and 8.8.8.8  
10. `09_nslookup_after_fix.png`  nslookup google.com after DNS fix  
11. `10_ping_after_fix.png`  ping google.com after DNS fix  
12. `windows_ping.png`  ipconfig and ping google.com from Windows 10  
13. `windows_homescreen.png`  Windows 10 VM desktop

You can view these files in the screenshots folder in this repo.

---

## Skills Practiced

* Basic IT troubleshooting and support practices
* Working with the Linux command line  
* DNS and network fundamentals  
* Virtual machine setup in VirtualBox  
* Writing simple documentation with commands and screenshots

---

## Contact

Philip Muonaka  
phllaxel@hotmail.com  
[LinkedIn ](https://www.linkedin.com/in/chiedozie-philip-muonaka-53b554398/) 

