# Framework-spinner

## installation
**Backup your Plymouth themes folder**
```
sudo cp -r /usr/share/plymouth/themes/. /usr/share/plymouth/themes-bak/
```


**Clone the repository**
```
git clone https://github.com/Player6734/Framework-spinner.git /home$USER/Downloads/framework-spinner
```

**cd into it**
```
cd /home/$USER/Downloads/framework-spinner
```

**Remove old throbber files**

Note: This step might vary depending on your theme setup. Check if your Plymouth theme contains a 'spinner' directory and manually verify the files to be deleted.
```
sudo find /usr/share/plymouth/themes/spinner -type f -name 'throbber-*' -delete
```

**Copy all of the throbber files to the 'spinner' folder of the plymouth theme** 

This copies the new throbber files to your Plymouth 'spinner' directory.
```
sudo cp -r frames/. /usr/share/plymouth/themes/spinner/
```

**Apply changes to the kernel**

Update the kernel to apply the changes. It is recommended to backup your kernel configuration as a precaution.
```
sudo dracut --force
```


### For fedora users
Since that's the distro i'm on i can confidently make a one copy-paste-action for this:

(all the commands above chained)
```
sudo cp -r /usr/share/plymouth/themes/. /usr/share/plymouth/themes-bak/ ; git clone https://github.com/Player6734/Framework-spinner.git /home$USER/Downloads/framework-spinner ; cd /home/$USER/Downloads/framework-spinner ; sudo find /usr/share/plymouth/themes/spinner -type f -name 'throbber-*' -delete ; sudo cp -r frames/. /usr/share/plymouth/themes/spinner/ ; sudo dracut --force ;
