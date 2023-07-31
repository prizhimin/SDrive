# SDrive Firmware and Soft

hex и eep - файлы прошивки
sdrive.atr - записать в корень SD-карты

Прошивка:
- во время прошивки все dip-переключатели должны быть внизу (разомкнуты), SD-карта не вставлена, питание 5 вольт подаётся
- прошивать в 2 захода: сначала flash (.hex) и фьюзы, потом eeprom (.eep)

Команда для прошивки: 
avrdude.exe -p m328p -U lfuse:w:0xfe:m -U hfuse:w:0xd8:m efuse:w:0xfc:m -c usbasp
