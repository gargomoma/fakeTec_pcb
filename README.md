# fakeTec_pcb
A low-cost nrf52 device with the form-factor of the heltec v2 & v3 devices.

The variant & design is based on the DIY
<a href="https://github.com/mrekin/MeshtasticCustomBoards/tree/main/firmware/variants/diy/promicro_diy_m" target="_blank">proMicro variant</a>.

As MCU board is used <a href="https://github.com/joric/nrfmicro/wiki/Alternatives#supermini-nrf52840l" target="_blank">ProMicro/SuperMini</a>

# Variants

(aka firmware files)

| Version | Lora Modules | Official Repo link | Unofficial Repo link |
| :------------ | :---------------------------- | :-----------------| :-----------------|
| With TXCO | EByte E22/E220-xxxM-22S/HT-RA62 | <a href="https://github.com/meshtastic/firmware/tree/master/variants/diy/nrf52_promicro_diy_tcxo" target="_blank">Official repo - With TXCO</a> | <a href="https://github.com/mrekin/MeshtasticCustomBoards/tree/main/firmware/variants/diy/promicro_diy_m" target="_blank">With TXCO</a> @mrekin/MeshtasticCustomBoards|
| Without TXCO | EByte E22/E220-xxxMM-22S/RA-01SH | <a href="https://github.com/meshtastic/firmware/tree/master/variants/diy/nrf52_promicro_diy_xtal" target="_blank">Official repo - Without TXCO</a> | <a href="https://github.com/mrekin/MeshtasticCustomBoards/tree/main/firmware/variants/diy/promicro_diy_mm" target="_blank">Without TXCO</a> @mrekin/MeshtasticCustomBoards|

You can use <a href="https://mrekin.duckdns.org/flasher/" target="_blank">mrekin's flasher</a>

# Bill of materials

| Part | Source | Cost&nbsp;(€) | Note |
| :------------ | :---------------------------- | :-----------------| :-----------------|
| ProMicro (aka NiceNano) | <a href="https://www.aliexpress.com/item/1005006446457448.html" target="_blank">Aliexpress</a> | 6€ ||
| HT-RA62 | <a href="https://www.aliexpress.com/item/1005005543917617.html" target="_blank">AliExpress</a> | 5€ | You can use Ra-01SH as well <a href="https://www.aliexpress.com/item/1005002561194884.html">Ra-01SH</a> |
| 2x Through Hole Resistors // SMD resistor | <a href="https://www.aliexpress.com/item/1005006044241818.html" target="_blank">Aliexpress</a> | 3€ pack<br /> 0.1€/resistor | You can buy a package of multiple values for a few €.<br /> Choose depending on material you already have &/or soldering skills. I'm using 2x 1M ohms|
| Battery connection (optional) | <a href="https://www.aliexpress.com/item/1005002564191148.html" target="_blank">AliExpress</a> | 2€ pack<br /> 0.4€/unit | This is an example.|
| Antenna pigtail (optional) | <a href="https://www.aliexpress.com/item/4001287491018.html" target="_blank">AliExpress</a> | 2€ | I saw that it underperformed whith a cheap black pigtail, after using one of these, it worked fine.|
| PCB |  | 2€ pack of 5<br /> 0.4€/unit | Use your favourite company to get the pcb.|
|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;||||
| <strong>Total</strong> || 11,9€ | |

# Notes

Check if the bootloader version is >0.8, update if needed from [here](https://github.com/adafruit/Adafruit_nRF52_Bootloader/releases)

Look for: "update-nice_nano_bootloader-X.X.X_nosd" where X.X.X is the version. Latest version is: [update-nice_nano_bootloader-0.9.1_nosd.uf2](https://github.com/adafruit/Adafruit_nRF52_Bootloader/releases/download/0.9.1/update-nice_nano_bootloader-0.9.1_nosd.uf2)

To flash all you need to do is to connect the device via USB and double tap reset, by double tap RST and GND pins with tweezers. After doing so you should see in your OS a USB storage device named "NICENANO". Copy/move the .uf2 file into the storage device and wait for the reboot.

# ♥Thanks♥
Thanks to all the folks in the [Discoord NRF52 chat](https://discord.com/channels/867578229534359593/1194757507013427250) for the support on designing this board ♥ 


# Pictures
| Front | Back |
| :------------ | :---------------------------- |
|![image](https://github.com/gargomoma/fakeTec_pcb/blob/main/pics/simulation_image_top.png) | ![image](https://github.com/gargomoma/fakeTec_pcb/blob/main/pics/simulation_image_bottom.png) |
