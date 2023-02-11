# This is a branch for hackintosh EFI
    
    12100F + JGINYUE B660i Snown Dream + AMD Radeon RX5600XT + Tiplus 2TB + DW1560/BCM94352Z
    
    * Working
    
    Ventura 13.2
    USB mapped with rear 2 USB3.0 ports unavailable
    Wi-Fi & Bluetooth normal
    Serial number generated
    VirtualSMC and sensors functinal
    Sleep
    
    * Not Working
    
   
```shell
# fix bluetooth power issue
sudo defaults write bluetoothaudiod "Enable AAC codec" -bool true
defaults write com.apple.BluetoothAudioAgent "Apple Bitpool Min (editable)" 35;defaults write com.apple.BluetoothAudioAgent "Apple Initial Bitpool Min (editable)" 53;defaults write com.apple.BluetoothAudioAgent "Apple Initial Bitpool (editable)" 35

``` 
