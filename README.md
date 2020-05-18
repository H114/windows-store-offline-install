# windows-store-offline-install
##tested on Windows 10 version 1709 and later (shuld work for before )##
works on any windows 10 
## To install, run Add-Store.cmd as Administrator  
If you do not want App Installer / Purchase App  delete each command line appxbundle before running to install. However, if you plan on installing games or any app with in-purchase options, you should include everything.  
## troubleshooting 1
If the store still will not function, reboot. If still not working, open the command prompt as the administrator and run the following command, then reboot once more.  
```PowerShell -ExecutionPolicy Unrestricted -Command "& {$manifest = (Get-AppxPackage Microsoft.WindowsStore).InstallLocation + '\AppxManifest.xml' ; Add-AppxPackage -DisableDevelopmentMode -Register $manifest}"```    
## troubleshooting 2
> search for
 WSReset.exe  then run it
This will clear store cache
