# iPhone-4s-SSH-RD
iPhone 4s SSH Ramdisk with full root access 
When checkm8 will support A5 devices this can bypass iCloud but for now it's for just managing all rootFS from ramdisk level

# Requirements:
usbmuxd (you can install with home brew)
You need to be Jailbroken 
OpenSSH
afc2

# Insctructions 
1. put kloader using iFunbox to / 
2. put patchediBSS using iFunbox to /
3. On Mac open terminal and write : ssh root@youripadress
4. chmod 777 /kloader
5. cd /
6. ./kloader /patchediBSS
7. Your iPhone should go black 
8. Press home button at once so itunes can recognize it
9. Your iPhone is in kDFU
10. clear terminal and write : ./irecovery -f iBEC.n94ap.RELEASE.dfu
11. ./irecovery_old -s
12. The shell should appear in irecovery
13. /send DeviceTree.n94ap.img3
14. devicetree
15. /send ssh_ramdisk
16. ramdisk
17. /send kernelcache.release.n94
18. bootx
19. now device should boot verbosely and after it should show restore progress
20. now : ./iproxy 2222 22
21. in second terminal window write : ssh root@localhost -p2222
22. DONE !!!! YOU CAN ENJOY YOUR ROOT COMMANDS AND YOU CAN ENJOY EXPLORING FILESYSTEM FOR EXAMPLE VIA CYBERDUCK

# Credits 
Thanks to @Arsevka_JDM for helping me with this 

