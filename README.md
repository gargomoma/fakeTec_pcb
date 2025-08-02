# fakeTec_pcb
A low-cost nRF52 device with the form-factor of the Heltec v2 & v3 devices compatible with [Meshtastic](https://meshtastic.org/)®.

# Pictures
<details><summary>Click to open</summary>

| Front | Back |
| :------------ | :---------------------------- |
|![image](https://github.com/gargomoma/fakeTec_pcb/blob/main/pics/front_fakeTec.png) | ![image](https://github.com/gargomoma/fakeTec_pcb/blob/main/pics/back_fakeTec.png) |

</details>

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
| ProMicro (aka NiceNano) | <a href="https://www.aliexpress.com/item/1005006446457448.html" target="_blank">AliExpress</a><br /> <a href="https://www.aliexpress.com/item/1005007738886550.html" target="_blank">AliExpress</a> | 5€ <br /> 2x for 5€ | ⚠️[Please read it before buying red ProMicros](https://github.com/gargomoma/fakeTec_pcb/issues/30)⚠️ |
| HT-RA62 | <a href="https://www.aliexpress.com/item/1005005543917617.html" target="_blank">AliExpress</a> | 5€ | You can also use <a href="https://www.aliexpress.com/item/1005002561194884.html">RA-01SH</a> |
| 2x Through Hole Resistors // SMD resistor | <a href="https://www.aliexpress.com/item/1005006044241818.html" target="_blank">AliExpress</a> | 3€ pack<br /> 0.1€/resistor | You can buy a package of multiple values for a few €.<br /> Choose depending on material you already have &/or soldering skills. I'm using 2x 1M ohms |
| OLED SSD1306 i2c (optional) | <a href="https://www.aliexpress.com/item/1005005970901119.html" target="_blank">AliExpress</a> | 1.5€ | No need to solder, just be careful and add some tape in between the boards to avoid a short. |
| Battery connection (optional) | <a href="https://www.aliexpress.com/item/1005002564191148.html" target="_blank">AliExpress</a> | 2€ pack<br /> 0.4€/unit | This is an example. |
| Antenna pigtail (recommended) | <a href="https://www.aliexpress.com/item/4001287491018.html" target="_blank">AliExpress</a> | 2€ | I saw that it underperformed with a cheap black pigtail, after using one of these, it worked fine. |
| PCB |  | 2€ pack of 5<br /> 0.4€/unit | Use your favourite company to get the PCB. |
| 2x Buttons | <a href="https://www.aliexpress.com/item/4001125532910.html" target="_blank">AliExpress</a> | 1.8€ pack<br /> 0.1€/button | You can buy a package of 100 for a few €.<br /> I couldn't find a part code, search for "3*4*2.0 2 Pin Button" |
| [#16](https://github.com/gargomoma/fakeTec_pcb/issues/16) lupusworax's v4<br /> Mosfets SI2312 | <a href="https://www.aliexpress.com/item/1005004676217612.html" target="_blank">AliExpress</a> | 9€ pack of 200<br /> | --- |
| [#16](https://github.com/gargomoma/fakeTec_pcb/issues/16) lupusworax's v4<br /> Resistors | <a href="https://www.aliexpress.com/item/1005002991902748.html" target="_blank">AliExpress</a> | 2.4€ pack of 100<br /> | --- |
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;||||
| <strong>Total</strong> || 10€ | |

# Community contributions

| Author | Name | Link |
| :------------ | :------------ | :---------------------------- |
| [lupusworax](https://github.com/gargomoma/fakeTec_pcb/issues/8) | **FakeCAP** | [printables](https://www.printables.com/model/1067553-meshtastic-fakecap-super-slim-nrf52-gps-node) |
| [lupusworax](https://github.com/gargomoma/fakeTec_pcb/issues/34) | **FakeCAP Solar** | [printables](https://www.printables.com/model/1299801-fakecap-solar-maximus-faketec-meshtastic-node) |
| [lupusworax](https://github.com/gargomoma/fakeTec_pcb/issues/8) | **Tamameshi** | [printables](https://www.printables.com/model/1061194-lwc-meshtastic-tamameshi-portable-faketec-node) |
| [lupusworax](https://github.com/gargomoma/fakeTec_pcb/issues/8) | **Meshformer** | [printables](https://www.printables.com/model/1058668-lwc-meshtastic-meshformer-communicator-node) |
| [lupusworax](https://github.com/gargomoma/fakeTec_pcb/issues/8) | **WayPoint** | [printables](https://www.printables.com/model/1104742-meshtastic-waypoint-water-resistant-outdoor-solar) |
| [lupusworax](https://github.com/gargomoma/fakeTec_pcb/issues/8) | **MeshTAK** | [printables](https://www.printables.com/model/1116459-meshtastic-meshtak-tacticool-big-boi-water-resista) |
| [lupusworax](https://github.com/gargomoma/fakeTec_pcb/issues/8) | **SCOUT** | [printables](https://www.printables.com/model/1144370-meshtastic-faketak-scout-ultra-portable-tacticool) |
| [lupusworax](https://github.com/gargomoma/fakeTec_pcb/issues/8) | **F1 Micro** | [printables](https://www.printables.com/model/1123408-meshtastic-faketec-f1-micro-node-nrf52) |
| [lupusworax](https://github.com/gargomoma/fakeTec_pcb/issues/34) | **Amade 2 ( Duo color vintage)** | [printables](https://www.printables.com/model/1286551-meshtastic-faketec-amade2-nrf52-node-duo-color-vin) |
| [lupusworax](https://github.com/gargomoma/fakeTec_pcb/issues/8) | **Solar Outdoor Node Remix** | [printables](https://www.printables.com/model/1302410-faketec-solar-outdoor-node) |
| [mosstrike1](https://cults3d.com/en/users/mosstrike1) | **FakeDeck** | [cults3d](https://cults3d.com/en/3d-model/various/fakedeck-a-faketek-standalone-meshtastic-device ) |
| [candre23](https://github.com/gargomoma/fakeTec_pcb/issues/5) | **Dummy Model** | [printables](https://www.printables.com/model/1098558-faketec-dummy-model) |
| [candre23](https://github.com/gargomoma/fakeTec_pcb/issues/5) | **p4gr** | [printables](https://www.printables.com/model/1099391-p4gr-a-minimalist-enclosure-for-the-faketec-meshta) |
| [lastparody](https://github.com/gargomoma/fakeTec_pcb/issues/40) | **Testosterone Edition Case**| [makerworld](https://makerworld.com/tr/models/1646395-faketec-case-testosterone-edition) |

## Videos
[Building FakeTec v2 by KBOX Labs](https://www.youtube.com/watch?v=NtnSVTl6weA)

[Building FakeTec v2 by lupusworax](https://www.youtube.com/watch?v=JvBfYyUF-0w)

[Building FakeTec v3 by ea3grn (spanish)](https://www.youtube.com/watch?v=NRIXPWYmfq8)

## Blog posts

[Building guide by Adrelien](https://adrelien.com/diy-meshtastic-how-to-build-your-own-meshtastic-device-with-faketec-pcb-nrf52840)

## PCB Versions

| Version | Author | Description |
|--------|--------|--------|
| 1 | gargomoma | Original layout. |
| 2 | gargomoma | OledPins moved; Voltage divider resistors moved; added 2mm holes. |
| 3 | gargomoma | Bigger pads; Added 2 x pushbuttons; Access to charge boost option. |
| [4](https://github.com/gargomoma/fakeTec_pcb/issues/16) * | lupusworax | Same as v3 with 3 x smd power mosfets for swithching external hardware.|
| [5](https://github.com/gargomoma/fakeTec_pcb/issues/24) * | ShimonHoranek | Battery protection, low profile, JST connector, dedicated battery pins.|
| [6](https://github.com/gargomoma/fakeTec_pcb/issues/26) * | ShimonHoranek | ⚠️UNTESTED⚠️ Similar to v5 + SOLAR (CN3791 MPPT).|

* The Gerber files in the repository may not be the most recent. Always verify the user's original post for updates before using a community-submitted design.

Hint: Newer versions aren't necessarily superior; when unsure use v3 or v4.

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

# About Meshtastic
[Meshtastic](https://meshtastic.org/)® is a registered trademark of Meshtastic LLC. Meshtastic software components are released under various licenses, see github for details.

# Disclaimer
No warranty is provided.
You use it at your own risk and take the responsibility upon yourself.
