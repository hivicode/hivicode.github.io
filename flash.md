taruh semua file (boot dan rom) yang dibutuhkan ke folder platform tools

1. boot ke fastboot
   - tekan lama power dan volume down
     atau
   - buka folder platform tools, buka di terminal, sambungkan hp dengan usb dan ketik
   ```bash
   .\adb reboot bootloader
   ```

2. ketika sudah di bootloader atau fastboot, cek connect dengan
   ```bash
   .\fastboot devices
   ```
  
4. flash file boot
   ```bash
   .\fastboot flash boot boot.img
   ```
   
5. reboot ke recovery
   ```bash
   .\fastboot reboot recovery
    ```
   
6. Factory reset
   lakukan factory reset &/ format data

7. Install rom / apply update
   - di menu utama recovery pilih apply update (kalau rom ada di sdcard pilih sdcard)
     jika rom ada di folder platform tools pilih adb dan ketik ini
   ```bash
   adb sideload "nama rom.zip"
   ```
   (tanpa tanda petik)
   biasanya stuck tapi bakal berhasil atau sukses jika sudah ada tulisan total xfer...
