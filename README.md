# fakeTec_pcb
A low-cost nRF52 device with the form-factor of the Heltec v2 & v3 devices compatible with [Meshtastic](https://meshtastic.org/)®.

## Features
- Small size based on Heltec v3: You can use the same cases!
- i2c side ports ready to connect an OLED SSD1306 screen.
- Battery sensing: You can use SMD resistors or through-hole.
- 2mm mounting holes.
- Compatible with HT-RA62 / RA-01SH LoRa modules (and probably others with similar footprint).
- The variant & design is based on the DIY
<a href="https://github.com/mrekin/MeshtasticCustomBoards/tree/main/firmware/variants/diy/promicro_diy_m" target="_blank">ProMicro variant</a>.
- As MCU board its used <a href="https://github.com/joric/nrfmicro/wiki/Alternatives#supermini-nrf52840l" target="_blank">ProMicro/SuperMini</a>

# Variants

(aka firmware files)

| Version | Lora Modules | Official Repo link | Unofficial Repo link |
| :------------ | :---------------------------- | :-----------------| :-----------------|
| With TCXO | EByte E22/E220-xxxM-22S/HT-RA62 | <a href="https://github.com/meshtastic/firmware/tree/master/variants/diy/nrf52_promicro_diy_tcxo" target="_blank">Official repo - With TCXO</a> | <a href="https://github.com/mrekin/MeshtasticCustomBoards/tree/main/firmware/variants/diy/promicro_diy_m" target="_blank">With TCXO</a> @mrekin/MeshtasticCustomBoards|
| Without TCXO | EByte E22/E220-xxxMM-22S/RA-01SH | <a href="https://github.com/meshtastic/firmware/tree/master/variants/diy/nrf52_promicro_diy_xtal" target="_blank">Official repo - Without TCXO</a> | <a href="https://github.com/mrekin/MeshtasticCustomBoards/tree/main/firmware/variants/diy/promicro_diy_mm" target="_blank">Without TCXO</a> @mrekin/MeshtasticCustomBoards|

ℹ️If you don't want to build your own image use <a href="https://mrekin.duckdns.org/flasher/" target="_blank">mrekin's flasher</a>

# Bill of materials

| Part | Source | Cost&nbsp;(€) | Note |
| :------------ | :---------------------------- | :-----------------| :-----------------|
| ProMicro (aka NiceNano) | <a href="https://www.aliexpress.com/item/1005006446457448.html" target="_blank">AliExpress</a> | 5€ ||
| HT-RA62 | <a href="https://www.aliexpress.com/item/1005005543917617.html" target="_blank">AliExpress</a> | 5€ | You can also use <a href="https://www.aliexpress.com/item/1005002561194884.html">RA-01SH</a> |
| 2x Through Hole Resistors // SMD resistor | <a href="https://www.aliexpress.com/item/1005006044241818.html" target="_blank">AliExpress</a> | 3€ pack<br /> 0.1€/resistor | You can buy a package of multiple values for a few €.<br /> Choose depending on material you already have &/or soldering skills. I'm using 2x 1M ohms |
| OLED SSD1306 i2c (optional) | <a href="https://www.aliexpress.com/item/1005005970901119.html" target="_blank">AliExpress</a> | 1.5€ | No need to solder, just be careful and add some tape in between the boards to avoid a short. |
| Battery connection (optional) | <a href="https://www.aliexpress.com/item/1005002564191148.html" target="_blank">AliExpress</a> | 2€ pack<br /> 0.4€/unit | This is an example. |
| Antenna pigtail (recommended) | <a href="https://www.aliexpress.com/item/4001287491018.html" target="_blank">AliExpress</a> | 2€ | I saw that it underperformed with a cheap black pigtail, after using one of these, it worked fine. |
| PCB |  | 2€ pack of 5<br /> 0.4€/unit | Use your favourite company to get the PCB. |
| 2x Buttons | <a href="https://de.aliexpress.com/item/4001125532910.html" target="_blank">AliExpress</a> | 1.8€ pack<br /> 0.1€/button | You can buy a package of 100 for a few €.<br /> I couldn't find a part code, search for "3*4*2.0 2 Pin Button" |
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;||||
| <strong>Total</strong> || 10€ | |

# Notes

### Bootloader
>Check if the bootloader version is >0.8, update if needed from [here](https://github.com/adafruit/Adafruit_nRF52_Bootloader/releases)
>
>Look for: "update-nice_nano_bootloader-X.X.X_nosd" where X.X.X is the version.
>
>Latest version is: [update-nice_nano_bootloader-0.9.2_nosd.uf2](https://github.com/adafruit/Adafruit_nRF52_Bootloader/releases/download/0.9.2/update-nice_nano_bootloader-0.9.2_nosd.uf2)
>
>To flash all you need to do is to connect the device via USB and double tap RST and GND pins with tweezers. After doing so you should see in your OS a USB storage device named "NICENANO". Copy/move the .uf2 file into the storage device and wait for the reboot.
>
>If you cannot do this, consider the board came without bootloader, keep reading to know how to flash it.

### Charging current
>If you plan to charge the batteries, remember you can increase the charging current by bridging the _boost_ pads at the bottom of the proMicro board.
>You'll find more info on AliExpress listing, and also <a href="https://github.com/joric/nrfmicro/wiki/Alternatives#supermini-nrf52840l" target="_blank">here</a>.
>

### My ProMicro is dead. What can i do?
##### ⚠️ALWAYS TEST THE ProMicros BEFORE SOLDERING!⚠️
>Some sellers sell the ProMicros for very very cheap, but they don't provide bootloader (so you basically got a very smol brick), no problem.

Download the .hex bootloader from [here](https://github.com/adafruit/Adafruit_nRF52_Bootloader/releases) and prepare an ESP32 with the instructions provided [here](https://github.com/atc1441/ESP32_nRF52_SWD).

Latest .hex bootloader is [nice_nano_bootloader-0.9.2_s140_6.1.1.hex](https://github.com/adafruit/Adafruit_nRF52_Bootloader/releases/download/0.9.2/nice_nano_bootloader-0.9.2_s140_6.1.1.hex).

Once you got the ESP32 board ready, solder `CLK`,`DIO`,`GND`,`VDD` (or the `3v`) to the corresponding pins on the ESP32. (The ProMicro pins are on the back of the board.)

Then:
 1. Power the ESP32 on, on your browser open swd.local (or the IP assigned)
 2. Click Init SWD (if the "Status" shows not okay, check the wiring)
 3. Erase nRF -> Ok: Everything erased (if nRF info mentions locked, erase & reset)
 4. Flash Uploaded File -> Select file (the .hex bootloader), offset = 0
 5. Flash uploaded File; Wait for the upload to complete.
 6. 🧟‍♀️IT'S ALIVEEEE🧟‍♀️

# ♥Thanks♥
Thanks to all the folks in the [Discord nRF52 chat](https://discord.com/channels/867578229534359593/1194757507013427250) for the support on designing this board ♥
And thank you to the people contributing with their own designs (see Community contributions).

# Pictures
| Front | Back |
| :------------ | :---------------------------- |
|![image](https://github.com/gargomoma/fakeTec_pcb/blob/main/pics/front_fakeTec.png) | ![image](https://github.com/gargomoma/fakeTec_pcb/blob/main/pics/back_fakeTec.png) |

# Community contributions
**[lupusworax](https://github.com/lupusworax)**'s [designs](https://github.com/gargomoma/fakeTec_pcb/issues/8).

| Name | Link |
| :------------ | :---------------------------- |
| **FakeCAP** | [https://www.printables.com/model/1067553-meshtastic-fakecap-super-slim-nrf52-gps-node](https://www.printables.com/model/1067553-meshtastic-fakecap-super-slim-nrf52-gps-node) |
| **Tamameshi** | [https://www.printables.com/model/1061194-lwc-meshtastic-tamameshi-portable-faketec-node](https://www.printables.com/model/1061194-lwc-meshtastic-tamameshi-portable-faketec-node) |
| **Meshformer** | [https://www.printables.com/model/1058668-lwc-meshtastic-meshformer-communicator-node](https://www.printables.com/model/1058668-lwc-meshtastic-meshformer-communicator-node) |
| **WayPoint** | [https://www.printables.com/model/1104742-meshtastic-waypoint-water-resistant-outdoor-solar](https://www.printables.com/model/1104742-meshtastic-waypoint-water-resistant-outdoor-solar) |
| **MeshTAK** | [https://www.printables.com/model/1116459-meshtastic-meshtak-tacticool-big-boi-water-resista](https://www.printables.com/model/1116459-meshtastic-meshtak-tacticool-big-boi-water-resista) |

**[mosstrike1](https://cults3d.com/en/users/mosstrike1)**'s FakeDeck

[https://cults3d.com/en/3d-model/various/fakedeck-a-faketek-standalone-meshtastic-device](https://cults3d.com/en/3d-model/various/fakedeck-a-faketek-standalone-meshtastic-device )

**[candre23](https://github.com/candre23)**'s [dummy model](https://github.com/gargomoma/fakeTec_pcb/issues/5) + [case]()

| Name | Link |
| :------------ | :---------------------------- |
| **Dummy Model** | [https://www.printables.com/model/1098558-faketec-dummy-model](https://www.printables.com/model/1098558-faketec-dummy-model) |
| **p4gr** | [https://www.printables.com/model/1099391-p4gr-a-minimalist-enclosure-for-the-faketec-meshta](https://www.printables.com/model/1099391-p4gr-a-minimalist-enclosure-for-the-faketec-meshta) |



# About Meshtastic
[Meshtastic](https://meshtastic.org/)® is a registered trademark of Meshtastic LLC. Meshtastic software components are released under various licenses, see github for details.

# Disclaimer
No warranty is provided.
You use it at your own risk and take the responsibility upon yourself.
