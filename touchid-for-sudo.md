Taken from: https://dev.to/siddhantkcode/enable-touch-id-authentication-for-sudo-on-macos-sonoma-14x-4d28


Steps to Enable Touch ID for sudo
1. Create and Edit the Configuration File
Create a new configuration file based on the template provided in macOS Sonoma.
```
sudo cp /etc/pam.d/sudo_local.template /etc/pam.d/sudo_local
```

2. Edit the newly created file with your preferred text editor:


```
sudo vim /etc/pam.d/sudo_local
```

3. In the file, locate the following line, Uncomment it by removing the #:


```
- #auth       sufficient     pam_tid.so
+ auth       sufficient     pam_tid.so
```


4. Confirm the Operation
Open a new terminal session and run a sudo command to test the setup:

```
sudo ls
```