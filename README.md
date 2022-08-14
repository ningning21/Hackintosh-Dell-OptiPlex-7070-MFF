# Hackintosh-OptiPlex-7070-MFF-intel

> based on https://github.com/webleon/Hackintosh-OptiPlex-7070-MFF

![](https://raw.githubusercontent.com/ningning21/Hackintosh-Dell-OptiPlex-7070-MFF/main/Images/big-sur.png)

**Opencore Bootloader 0.7.4. opencore configurator 2.51.00. Tested on Big sur 11.x and Monterey 12.0.1 , but bluetooth is not work


## Introdution
This is the Hackintosh EFI Folder for Dell OptiPlex 7070 Micro Form Factor. 

You will have to [**generate a new SMIBIOS**](https://github.com/corpnewt/GenSMBIOS) before login to your iCloud account.


## Hardware Specs
* **Desktop Computer**: [Dell OptiPlex 7070 Micro Form Factor 65W](https://www.dell.com/tc/business/p/optiplex-7070-micro/pd) 
* **CPU**: [Intel® Core™ i7-9700](https://ark.intel.com/content/www/us/en/ark/products/191792/intel-core-i7-9700-processor-12m-cache-up-to-4-70-ghz.html)
* **iGPU**: Intel® UHD Graphics 630
* **RAM**: 14GB DDR4 2666 Daul Channel
* **HDD**: TOSHIBA RD500 NVMe SSD 500G
* **LAN**: Realtek RTL8125B / Intel I219LM7
* **Wi-Fi & Bluetooth**: intel ac9560 160hz


## Working
* CPU Turbo Boost & Thermal Throttling
* Dual Display up to 4k60Hz
* iGPU acceleration
* Front panel Headset (install ComboJack to enable Mic) and Line-out
* All USB Ports
* LAN & Wireless Network
* Sleep & Wakeup


## Not working
* Airdrop & Airplay
* bluetooth (on Monterey)

## BIOS Settings
* General → Advanced Boot Options: ***uncheck***
* System Configuration → SATA Operation: ***AHCI***
* Secure Boot → Secure Boot Enable: ***Disabled***
* Intel® Software Guard Extensions™ → Intel® SGX™ Enable: ***Disabled***
* Virtualization Support → VT for Direct I/O: ***uncheck***


## BIOS Settings via GRUB
* Set Pre-Allocated DVMT to 64M: 
***setup_var 0x8DC 0x02***
* Disable CFG lock: 
***setup_var 0x5BE 0x00***
