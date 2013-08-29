## Phone

### Wipe Phone

    ./fastboot erase system
    ./fastboot erase data
    ./fastboot erase cache
    
### Lock Phone (wipes data)

    ./fastboot oem lock
    
### Unlock Phone (wipes data)

    ./fastboot oem unlock
    
### Rebuild Phone (using maguro 4.2.2 as example)

unlock phone to gain full permissions

    ./fastboot oem unlock
    
flash bootloader, reboot, radio baseband, reboot, install new 4.2.2 o/s

    ./fastboot flash bootloader bootloader-maguro-primelc03.img
    ./fastboot reboot-bootloader
    ./fastboot flash radio radio-maguro-i9250xxlj1.img
    ./fastboot reboot-bootloader
    ./fastboot -w update image-yakju-jdq39.zip

lock phone afterwards

    ./fastboot oem lock

reboot and enjoy

    ./fastboot reboot-bootloader

## Tablet (nexus 7)

    ./fastboot oem unlock
    ./fastboot erase boot
    ./fastboot erase cache
    ./fastboot erase recovery
    ./fastboot erase system
    ./fastboot erase userdata
    ./fastboot flash bootloader bootloader-grouper-4.23.img
    ./fastboot reboot-bootloader 
    ./sleep 10
    ./fastboot -w update image-nakasi-jwr66v.zip
    ./fastboot oem lock

Had problems updating the bootloader for the nexus 7 2012 wifi edition, managed to find a verified bootloader 4.23 that works, in /bootloader dir

### Factory Images

[https://developers.google.com/android/nexus/images](https://developers.google.com/android/nexus/images)

### Notes

Galaxy Nexus from Wind runs on "yakju" for Galaxy Nexus "maguro" (GSM/HSPA+). Download JDQ39 build 4.2.2
