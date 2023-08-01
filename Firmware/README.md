# SDrive Firmware and Soft

hex и eep - файлы прошивки

sdrive.atr - записать в корень SD-карты

Прошивка:
- во время прошивки все dip-переключатели должны быть внизу (разомкнуты), SD-карта не вставлена, питание 5 вольт подаётся
- прошивать в 2 захода: сначала flash (.hex) и фьюзы, потом eeprom (.eep)

Программатор USBasp с Aliexpress

Программируем при помощи avrdude https://github.com/avrdudes/avrdude

Команда для прошивки фьзов: 
avrdude.exe -p m328p -U lfuse:w:0xfe:m -U hfuse:w:0xd8:m efuse:w:0xfc:m -c usbasp


---------------------------------------------------------------

hex and eep firmware files

sdrive.atr - write to the root of the SD card

Firmware:

during the firmware, all dip switches must be at the bottom (open), the SD card is not inserted, 5 volts of power is supplied

to flash in 2 passes: first flash (.hex) and fuses, then eeprom (.eep)

The USBasp programmer with Aliexpress is programmed using avrdude https://github.com/avrdudes/avrdude

The command for the firmware of the fzs: avrdude.exe -p m328p -U lfuse:w:0xfe:m -U hfuse:w:0xd8:m efuse:w:0xfc:m -c usbasp