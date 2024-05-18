# install JDK => Java Development Kit
```sh
# download jdk 17
wget https://download.oracle.com/java/17/latest/jdk-17_linux-x64_bin.deb

# install it
sudo dpkg -i jdk-17_linux-x64_bin.deb

# configure it if you have multiple versions

sudo update-alternatives --config java

```

# Android SDK command-line tools
```sh
# go here
site: https://developer.android.com/studio
# scroll down till you see command line tools only
# pickup Linux Platform and download 
# unzip it
mkdir ~/android-sdk
# move it to android-sdk 
# copy alfiles into latest folder 
# ~/android-sdk/cmdline-tools/latest/
# add it to ~/.bashrc

#  install platform-tools platforms;android-34   build-tools;34.0.0
sdkmanager "platform-tools" "platforms;android-34" "build-tools;34.0.0"

# add platform-tools and build-tools 
# run sdkmanager --list 
sdkmanager --list

# install abd i installed api 34 so 
sdkmanager "system-images;android-34;default;x86_64"
# add emulator to the path variable 
# create an image when you download it 
avdmanager create avd -n testDevice -k "system-images;android-34;default;x86_64"
# start the emulator 
emulator @testDevice 
# 🚀 We are rockets


```
 

# Android NDK => Native Development Kit => add it to your system path
```sh 
# to to this link and download NDK for Linux 
site: https://developer.android.com/ndk/downloads
# unzip it and move it inside directory ~/android-sdk/ndk 
# add it to the path variable

```


# Install Flutter SDK 
# download it from
```sh 
site: https://docs.flutter.dev/get-started/install/linux/android?tab=download

mkdir ~/development 
mv ~/Downloads/flutter_linux_3.22.0-stable.tar.xz ~/development 
tar -xJvf flutter_linux_3.22.0-stable.tar.xz
rm flutter_linux_3.22.0-stable.tar.xz
# add it to the path variables
# 
exprt PATH="$HOME/development/flutter/bin:$PATH"
# flutter doctor 
flutter doctor 

# may will ask you for "Some Android licenses not accepted. To resolve this, run: flutter doctor --android-licenses"
flutter doctor --android-licenses
```
# you are now ready to start develop with flutter🚀
