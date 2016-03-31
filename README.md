# ios-usbmux-tunnel

A tunnel program to make connections via iOS's usbmux mechanism, using TCP with ports that can be specified.

### Usage

`` usbmux-tunnel --tunnel [--iport <iOS port>] [--lport <Local port>] ``

`` usbmux-tunnel --autoboot `` Exits iOS recovery mode.

`` usbmux-tunnel [--ibss <iBSS file>] [--exploit <iBSS USB exploit payload>] `` Loads an iBSS exploit

```
  [--ibec <iBEC file>] [--ramdisk <ramdisk file>]
  [--devicetree <devicetree file>] [--kernelcache <kernelcache file>]
  [--ramdisk-command <command to execute after sending ramdisk, default is 'ramdisk'>]
  [--ramdisk-delay <delay before loading ramdisk, in seconds, default is 5>]
  [--go-command <command to execute after sending iBEC, default is 'go'>]
  [--verbose <verbose level>]
```
			
### Examples:

`` usbmux-tunnel --lport 2022 ``

`` usbmux-tunnel --ibec iBEC_file_from_custom_FW --ramdisk created_ramdisk.dmg.ssh --devicetree DevicetreeXXX.img3 --kernelcache kernelcache_file_from_custom_FW --ramdisk-command "ramdisk 0x90000000" ``

The default ports used are 22 (iOS Device) <-> 2022 (OS X) or 22 (Windows)
