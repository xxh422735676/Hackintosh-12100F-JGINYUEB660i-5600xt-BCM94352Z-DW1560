# This is a repo for hackintosh EFI
    
**12100F + JGINYUE B660i Snown Dream + AMD Radeon RX5600XT + Tiplus 2TB + DW1560/BCM94352Z**
    
* Working
    
Ventura 13.2
USB mapped with rear 2 USB3.0 ports unavailable
Wi-Fi & Bluetooth normal
Serial number generated
VirtualSMC and sensors functinal
Sleep

* Not Working

NULL

**[IMPORTANT]** **use at your own risk. change your SMBIOS id, serial number and other platform-specific settings on your own PC.**
    
## Fix bluetooth power issue

```shell
sudo defaults write bluetoothaudiod "Enable AAC codec" -bool true
defaults write com.apple.BluetoothAudioAgent "Apple Bitpool Min (editable)" 35;defaults write com.apple.BluetoothAudioAgent "Apple Initial Bitpool Min (editable)" 53;defaults write com.apple.BluetoothAudioAgent "Apple Initial Bitpool (editable)" 35

``` 

## Fix CPU Turbo Frequency

```shell
# download CPUFriend.kext
# set currect SMBIOS ID
# get Board-id from Hackintool
./ResourceConverter.sh --kext /System/Library/Extensions/IOPlatformPluginFamily.kext/Contents/PlugIns/X86PlatformPlugin.kext/Contents/Resources/[Board-id].plist
```
put `CPUFriendProvider.kext`,`CPUFriend.kext` into `kext` folder and enabled

## Fix Bluetooth address NULL && USBcustomization

[Customize USB under windows](https://blog.csdn.net/Z17362251225/article/details/125540982)

## Fix Bluetooth && Wi-Fi
Read manual && select specific kexts carefully [BrcmPathRAM](https://github.com/acidanthera/BrcmPatchRAM)
Add this to kext [AirportBrcmFixup](https://github.com/acidanthera/AirportBrcmFixup)

## Fix sleep issue

Using method 1 patch [黑苹果睡眠自己突然醒来？或者睡了立马就醒？](https://www.bilibili.com/read/cv15048436)
[xjn819's blog](https://blog.xjn819.com/post/opencore-guide.html#:~:text=%E8%BF%99%E7%BB%84%E6%94%B9%E5%90%8D%E6%98%AF%E5%AF%B9%20XHC%20%E4%B8%8B%E7%9A%84%20PRW%20%E6%94%B9%E5%90%8D%E4%B8%BA%20xprw)



