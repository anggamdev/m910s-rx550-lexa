
# # DELL-OPTIPLEX-3020-MT-Hackintosh

Hackintosh for Build Up PC Dell Optiplex 3020 Mini Tower 

[![](https://github.com/anggamdev/DELL-OPTIPLEX-3020-MT-Hackintosh/blob/main/Hackintosh%20Dell%20Optiplex%203020%20Mini%20Tower.jpg)](https://github.com/anggamdev/DELL-OPTIPLEX-3020-MT-Hackintosh/blob/main/Hackintosh%20Dell%20Optiplex%203020%20Mini%20Tower.jpg//)


### Mode Boot :

- OpenCore
- macOS BigSur 11.7.10
- Mode : UEFI

### Sudah Test di Spek :
- Intel® H81 Chipset
- Processor Intel® Core™ i3-4150 Haswell / Core™ i5-4570 Haswell
- Integrated Intel® HD Graphics 4400 / 4600
- Storage : SSD SATA Colorfull 240GB
- Storage : Hardisk 2.5 Seagate 1TB 
- RAM : V-Gen 2x8GB DDR3 1600MHz
- Audio: Realtek ALC662
- Ethernet Card:  Realtek® RTL8151GD
- Bootloader OpenCore 0.9.7
- OS BigSur 11.7.10
- [Installer Olarila](https://www.olarila.com/topic/6278-olarila-vanilla-images-macos-installer/)



### Berkerja Normal  :
- QE/CI Intel® HD Graphics 4400 / 4600 Haswell
- Restart and Shutdown
- Sleep and Wake
- CPU Power Management
- Ethernet / Internet lewat LAN
- Audio Jack and Internal Mic (Depan & Belakang)
- Display Output : wajib pakai Display Port 
- Brightness : pakai [Monitor Control](https://github.com/MonitorControl/MonitorControl#readme "Monitor Control")
- Semua USB Ports
- Lainnya

### Tidak Berjalan / Bugs :-(

- Port d-Sub/VGA 

### [Download EFI](https://github.com/anggamdev/DELL-OPTIPLEX-3020-MT-Hackintosh/releases/tag/1) 

## CATATAN (WAJIB):
- Silakan buat SMBIOS dengan Tutorial [https://dortania.github.io/OpenCore-Install-Guide/extras/smbios-support.html#imac](http:https://dortania.github.io/OpenCore-Install-Guide/extras/smbios-support.html#imac// "https://dortania.github.io/OpenCore-Install-Guide/extras/smbios-support.html#imac")

## PENTING !!, WAJIB DILAKUKAN

- Boot ke drive USB. setelah masuk Menu Open Core, tekan tombol keyboard ke bawah, lalu klik Reset NVRAM
- Kemudian Reboot, dan masuk ke Menu Opencore lagi
- Lalu klik Select modGRUBShell.efi

Kemudian kamu masuk ke mode Shell seperti CMD , dan pastikan ada menu seperti dibawah :

```
grub>
``` 

dan masukan beberapa perintah dibawah ini :



### untuk Menonaktikan CFG Lock:

``` 
setup_var 0xD9E 0x0  
```

### Set DVMT (iGPU) ke 64MB

``` 
setup_var 0x263 0x2
``` 

### Untuk mengaktifkan EHCI hand-off
catatan : masukan satu persatu

``` 
setup_var 0x2 0x1
setup_var 0x144 0x1
setup_var 0x15A 0x2
setup_var 0x146 0x0
setup_var 0x147 0x0

```


### Reboot
kemudian reboot, dilanjutkan dengan ketik :

``` 
reboot
```
Setelah itu lanjut instalasi seperti biasa, bila ada pertanyaan silahkan DM



Thanks to varszegimarcell 
