# usb3_windowsXP_in_virtualbox

## Enable support USB3.0 in guest Windows XP on VirtualBox





* Download file Chipset_Driver_GVT5M_WN_3.0.23.0_A00.EXE from https://www.dell.com/support/home/en/en/debsdt1/drivers/driversdetails?driverid=gvt5m
* Select USB-3.0-Controller (xHCI) in your VM USB configuration
* Start Guest Windows Xp
* Run the downloaded file and choose unzipping
* click the button to open the folder with the unzipped files (...\Dell\drivers\Chipset_Driver_GVT5M_WN_3.0.23.0_A00)
* Run RENESAS-USB3-Host-Driver-30230-setup.exe to install the driver
* Shut down the Guest

### WINDOWS HOST:

>>> C:\Program Files\Oracle\VirtualBox\VBoxManage.exe" setextradata NameOfVM VBoxInternal/Devices/usb-xhci/0/Config/ChipType uPD720201

### LINUX HOST:

>>> vboxmanage setextradata NameOfVM VBoxInternal/Devices/usb-xhci/0/Config/ChipType uPD720201

* run guest



#### source: https://forums.virtualbox.org/viewtopic.php?t=91053