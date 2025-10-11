# Create Custom Windows Image

## Creating `.wim` File

Add a new disk to the VM

Use diskutil to initialize the disk with a fully allocated NTFS partition.

Setup Windows how you want it

Restart and select bootable usb/iso to get to repair menu

Use shift + f10 to open cmd

Find windows and `DATA` (secondary) drives:

```cmd
X:\sources>c:
C:\>dir
```

`c:` changes to the `C:\` partition, and `dir` lists the contents

> Note: the following commands assume windows is on C:\ and DATA is on D:\

Execute the following command to create `install.win` file

> Note: The `Description` is only required if you keep users for some reason

```cmd
dism /capture-image /imagefile:D:\install.wim /capturedir:C:\ /Name:windows11 /Description:"Your description"
```

Once complete, exit `cmd` and then continue into windows

Next install AnyBurn and download your source iso to your VM. 

Then run the program and select "Edit Image". Navigate to your source iso.


