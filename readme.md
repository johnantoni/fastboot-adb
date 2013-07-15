## Wipe Phone

    ./fastboot erase system
    ./fastboot erase data
    ./fastboot erase cache
    
## Lock Phone (wipes data)

    ./fastboot oem lock
    
## Unlock Phone (wipes data)

    ./fastboot oem unlock
    
## Rebuild Phone (using maguro 4.2.2 as example)

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

## Factory Images

[https://developers.google.com/android/nexus/images](https://developers.google.com/android/nexus/images)

