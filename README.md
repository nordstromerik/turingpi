# turingpi

## Flash CM4
Raspberry Pi are special and cannot be flashed using the gui like the RK1.
That is due to configuration needed to be done to the image, use raspberry imager
Set the slot in correct mode, device. Can be done via the turing pi GUI.
Use a usb A to usb A to connect to the turing board usb contact (white)

### Method 1
Connect your computer to the RPi MMC by issueing:
* cd "C:\Program Files (x86)\Raspberry Pi"  
* rpiboot -d .\msd
  
this "should" get you an mounted disc to flash the image to.
But probably won't!

### Method 2
ssh into the turing pi BMC:
* turing.local and login.
then issue commands:
*  tpi usb device -n x
*  tpi advanced msd --node x
*  tpi usb flash -n x
  
Where x is the slot number for the CM4 module.
