# Framework-spinner
Thank you sniss for making this gif!

## ![result](https://github.com/Player6734/Framework-plymouth/assets/88460695/3c80c32c-4990-404a-9f04-d06a1656e805) Installation ![result](https://github.com/Player6734/Framework-plymouth/assets/88460695/3c80c32c-4990-404a-9f04-d06a1656e805)
**Backup your Plymouth themes folder**
```
sudo cp -r /usr/share/plymouth/themes/. /usr/share/plymouth/themes-bak/
```


**Clone the repository**
```
git clone https://github.com/Player6734/Framework-plymouth.git /home/$USER/Downloads/framework-plymouth
```

**cd into it**
```
cd /home/$USER/Downloads/framework-plymouth
```

**Remove old throbber files**

Note: This step might vary depending on your theme setup. Check if your Plymouth theme contains a 'spinner' directory and manually verify the files to be deleted.
```
sudo find /usr/share/plymouth/themes/spinner -type f -name 'throbber-*' -delete
```

**Copy all of the throbber files to the 'spinner' folder of the plymouth theme** 

This copies the new throbber files to your Plymouth 'spinner' directory.
```
sudo cp -r Throbber-frames/. /usr/share/plymouth/themes/spinner/
```

**Apply changes to the kernel**

Update the kernel to apply the changes. It is recommended to backup your kernel configuration as a precaution.
```
sudo dracut --force -v
```

**Clean up the git repo downloaded**
```
rm -rf /home/$USER/Downloads/framework-plymouth
```

### For Fedora and OpenSUSE users
These are the two only distro where I've tested the commands. 
if the command `sudo find /usr/share/plymouth/themes/spinner -type f -name 'throbber-*'` outputs around 30 files then it should work.

(all the commands above chained)
```
sudo cp -r /usr/share/plymouth/themes/. /usr/share/plymouth/themes-bak/ ; git clone https://github.com/Player6734/Framework-plymouth.git /home/$USER/Downloads/framework-plymouth ; cd /home/$USER/Downloads/framework-plymouth ; sudo find /usr/share/plymouth/themes/spinner -type f -name 'throbber-*' -delete ; sudo cp -r Throbber-frames/. /usr/share/plymouth/themes/spinner/ ; cd ; sudo dracut --force -v ; rm -rf /home/$USER/Downloads/framework-plymouth
```

