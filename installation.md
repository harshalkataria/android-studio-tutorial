# Android studio installation
Here I am going to explain the process for installing android-studio from official archive on a 64-bit debian based linux OS.
## 1. Required Libraries
First, install 32-bit libraries for Android Studio installation  
`sudo apt-get update`  
`sudo apt install -y libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386`
## 2. Download Android studio
Next, open a browser and visit the below link to download the latest version of Android Studio from the official website.  
[Download](https://developer.android.com/studio)
## 3. Install
- Go to the `Downloads` directory or the directory where you have downloaded the Android Studio and then extract the downloaded archive using `tar` command.  
`tar -zxvf android-studio-ide-*-linux.tar.gz`  
`sudo mv android-studio /opt/`  
- Link the executable to `/bin` directory so that you can quickly start Android Studio using `android-studio` command.  
`sudo ln -sf /opt/android-studio/bin/studio.sh /bin/android-studio`  
- Create a `.desktop` file under `/usr/share/applications` directory to start Android Studio from Activities menu.  
`sudo nano /usr/share/applications/android-studio.desktop`  
- Use the following information in the above file.  
```
[Desktop Entry]
Version=1.0  
Type=Application  
Name=Android Studio  
Comment=Android Studio  
Exec=bash -i "/opt/android-studio/bin/studio.sh" %f  
Icon=/opt/android-studio/bin/studio.png  
Categories=Development;IDE;  
Terminal=false  
StartupNotify=true  
StartupWMClass=jetbrains-android-studio  
Name[en_GB]=android-studio.desktop
```
## 4. Access Android Studio
Start Android Studio by going to Activities » Search for Android Studio.
## 5. Reference
For more information: [Reference](https://www.itzgeek.com/post/how-to-install-android-studio-on-ubuntu-20-04/#:~:text=Install%20Android%20Studio%20From%20Official%20Archive,-First%2C%20install%2032&text=Go%20to%20the%20Downloads%20directory,downloaded%20archive%20using%20tar%20command.&text=Link%20the%20executable%20to%20%2Fbin,Studio%20using%20android%2Dstudio%20command.)
