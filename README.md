# Ebook_reader-TSC

## Pasi de implementare
1. Analiza documentatiei initiale
- Am urmarit schematicul si board layout-ul furnizate de profesor.
- Pe baza acestora, am reprodus designul electronic in Fusion Electronics, atat schematicul, cat si placa PCB.
2. Plasarea componentelor in PCB
- Am inceput sa asez componentele pe placa, respectand pozitionarea si orientarea optima pentru un traseu eficient si functional.
3. Rutarea traseelor
- Am efectuat manual rutarea traseelor de putere, pentru a ma asigura ca acestea sunt robuste si bine dimensionate.
- Pentru restul conexiunilor, am utilizat functia de autorouting pe ambele straturi: top si bottom.
- Am adaugat polygon pour pentru ambele straturi, pentru a realiza plane de masa.
4. Optimizarea layout-ului
- Am utilizat vias pentru a conecta planele de masa intre straturi si a completa zonele neconectate.
- Am aplicat via stitching pentru a imbunatati integritatea electrica.
5. Generarea modelului 3D al placii
- Am creat modelul 3D al placii pe baza designului 2D.
- Pentru aceasta, am cautat, descarcat si importat manual fiecare componenta 3D, apoi le-am pozitionat conform plasamentului din PCB-ul 2D.
- Pentru componenta test pad, nu am gasit un model 3D disponibil online, asa ca am fost nevoita sa il modelez manual, pentru a putea reprezenta corect placa in ansamblul 3D.
6. Integrarea in ansamblul final – Openbook Enclosure
- Am importat modelul 3D al placii in fisierul principal al carcasei: Openbook Enclosure.
- In acest fisier am plasat toate componentele in carcasa finala, astfel incat sa asigur o potrivire optima si functionala.
- Am desenat manual display-ul si bateria, pentru a le integra in ansamblu si a obtine o reprezentare cat mai realista a produsului final.

## Block Diagram

![Diagrama bloc](https://github.com/user-attachments/assets/405c5a0b-2344-4521-b1ab-5d89f00951f8)

## Bill of Materials
| Componenta | Link | Datasheet |
|-----------|--------------|-----------|
| Buton | [Model](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k) | [Datasheet](https://www.lcsc.com/datasheet/lcsc_datasheet_2201121800_PANASONIC-EVQPUJ02K_C2936858.pdf) |
| Capacitor | [Model](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO) | [Datasheet](//efaidnbmnnnibpcajpcglclefindmkaj/https://www.resistor.com/assets/pdf/0402tstd.pdf) |
| CPH3225A | [Model](https://www.snapeda.com/parts/CPH3225A/Seiko+Instruments/view-part/?ref=eda) | [Datasheet](https://octopart.com/datasheet/cph3225a-seiko-25340571) |
| EVQPUJ02K | [Model](https://industry.panasonic.com/global/en/products/control/switch/light-touch/number/evqpuj02k) | [Datasheet](https://www.lcsc.com/datasheet/lcsc_datasheet_2201121800_PANASONIC-EVQPUJ02K_C2936858.pdf) |
| KP-1608SURCK | [Model](https://www.snapeda.com/parts/KP-1608SURCK/Kingbright/view-part/?ref=search&t=LED%200603) | [Datasheet](//efaidnbmnnnibpcajpcglclefindmkaj/https://media.elv.com/file/107153_led_surck1608_data.pdf) |
| USBLC6-2SC6Y | [Model](https://www.snapeda.com/parts/USBLC6-2SC6Y/STMicroelectronics/view-part/?ref=eda) | [Datasheet](https://www.digikey.com/en/htmldatasheets/production/1375342/0/0/1/usblc6-2sc6y) |
| SD0805S020S1R0 | [Model](https://ro.mouser.com/ProductDetail/KYOCERA-AVX/SD0805S020S1R0?qs=jCA%252BPfw4LHbpkAoSnwrdjw%3D%3D) | [Datasheet](https://www.alldatasheet.com/view.jsp?Searchword=SD0805S&sField=2) |
| PGB1010603MR | [Model](https://www.snapeda.com/parts/PGB1010603MR/Littelfuse/view-part/?ref=eda) | [Datasheet](https://www.alldatasheet.com/view.jsp?Searchword=Pgb1010603mr&gad_source=1&gbraid=0AAAAADcdDU8aYfZtfJfdZ9I5j6RwZ_cbA&gclid=Cj0KCQjwqcO_BhDaARIsACz62vOPBOBe0eOh5gDUFkkKl4JBcbmoFZYtJ8BOnbaWqr_BuUCcVWvbutAaAmGkEALw_wcB) |
| BD5229G-TR  | [Model](https://componentsearchengine.com/part-view/BD5229G-TR/ROHM%20Semiconductor) | [Datasheet](https://www.lcsc.com/datasheet/lcsc_datasheet_2201131330_ROHM-Semicon-BD5229G-TR_C962636.pdf) |
| XC6220A331MR-G | [Model](https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex) | [Datasheet](https://www.alldatasheet.com/view.jsp?Searchword=Xc6220&gad_source=1&gbraid=0AAAAADcdDU8aYfZtfJfdZ9I5j6RwZ_cbA&gclid=Cj0KCQjwqcO_BhDaARIsACz62vPS06NB6tLgniZzfaVpKNu1m811BNk6AEPfg4DbP6f5S8QWA_pW_UQaAv-0EALw_wcB) |
| XC6220A331MR-G | [Model](https://componentsearchengine.com/part-view/XC6220A331MR-G/Torex) | [Datasheet](https://www.alldatasheet.com/view.jsp?Searchword=Xc6220&gad_source=1&gbraid=0AAAAADcdDU8aYfZtfJfdZ9I5j6RwZ_cbA&gclid=Cj0KCQjwqcO_BhDaARIsACz62vMO5_aHsn35cIZBK6oCFuB_WOxz_zKu4yOHJ69-EnaUd5Jfas_Avm8aAuk5EALw_wcB) |
| USB4110-GF-A  | [Model](https://componentsearchengine.com/part-view/USB4110-GF-A/GCT%20(GLOBAL%20CONNECTOR%20TECHNOLOGY)) | [Datasheet](//efaidnbmnnnibpcajpcglclefindmkaj/https://gct.co/files/drawings/usb4110.pdf) |
| Adafruit | [Model](https://eu.mouser.com/ProductDetail/Adafruit/4208?qs=PzGy0jfpSMtbScLbr0L5dw%3D%3D) | [Datasheet](https://www.arrow.com/en/manufacturers/adafruit-industries/datasheets) |
| Bobina | [Model](https://store.comet.srl.ro/Catalogue/Product/43497/) | [Datasheet](https://www.scribd.com/document/814581278/Datasheet-Bobina) |
| PFMF | [Model](https://www.mouser.co.uk/ProductDetail/EPCOS-TDK/B72520T0350K062?qs=dEfas%2FXlABIszF52uu7vrg%3D%3D) | [Datasheet](https://ro.mouser.com/c/ds/circuit-protection/thermistors/resettable-fuses-pptc/?m=Schurter&series=PFMF) |
| DMG2305UX-7 | [Model](https://componentsearchengine.com/part-view/DMG2305UX-7/Diodes%20Incorporated) | [Datasheet](//efaidnbmnnnibpcajpcglclefindmkaj/https://www.mouser.com/datasheet/2/115/DMG2305UX-266242.pdf?srsltid=AfmBOop22k34YTJJra1xubiU6LPiN4M4JlcWbRoSNdxSGFak8uWgXPpK) |
| Si1308EDL-T1-GE3 | [Model](https://componentsearchengine.com/part-view/SI1308EDL-T1-GE3/Vishay) | [Datasheet](https://www.alldatasheet.com/view.jsp?Searchword=Si1308edl&gad_source=1&gbraid=0AAAAADcdDU-px713ONYSnQ2O-gcwqYcFq&gclid=Cj0KCQjwqcO_BhDaARIsACz62vN_Nz3MJOc6J_03gnVBm7aSqC8v9wyP0VD-iRKP-gFrYgdhLi99I14aAlVJEALw_wcB) |
| R0402 | [Model](https://componentsearchengine.com/part-view/R0402%201%25%20100%20K%20(RC0402FR-07100KL)/YAGEO) | [Datasheet](//efaidnbmnnnibpcajpcglclefindmkaj/https://www.resistor.com/assets/pdf/0402tstd.pdf) |
| BME680 | [Model](https://www.snapeda.com/parts/BME680/Bosch/view-part/?welcome=home) | [Datasheet](//efaidnbmnnnibpcajpcglclefindmkaj/https://www.bosch-sensortec.com/media/boschsensortec/downloads/datasheets/bst-bme680-ds001.pdf) |
| SMD Solder | [Model](https://grabcad.com/library/solder-jumpers-1) | [Datasheet]() |
| W25Q512JVEIQ | [Model](https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda) | [Datasheet](//efaidnbmnnnibpcajpcglclefindmkaj/https://www.mouser.com/datasheet/2/949/W25Q512JV_SPI_RevB_06252019_KMS-2487502.pdf?srsltid=AfmBOoquExqDVgxEELF9CzuOGxHos0CD1nQDROHD6Eebdm2foNzqozqU) |
| ESP32-C6-WROOM-1-N8 | [Model](https://www.snapeda.com/parts/ESP32-C6-WROOM-1-N8/Espressif+Systems/view-part/?ref=eda) | [Datasheet](//efaidnbmnnnibpcajpcglclefindmkaj/https://www.mouser.com/catalog/specsheets/Espressif_ESP32_C6_WROOM_1%20_Datasheet_V0.1_PRELIMINARY_en.pdf?srsltid=AfmBOooHQKNitqODRaaPjoZInfWKTacDER1t5uRK6sKqT13TrzvVo_B7) |
| DS3231SN# | [Model](https://www.snapeda.com/parts/DS3231SN%23/Analog+Devices/view-part/?ref=eda) | [Datasheet](https://www.alldatasheet.com/view.jsp?Searchword=Ds3231sn%20datasheet&gad_source=1&gbraid=0AAAAADcdDU-Gy9URfMxGmqiPg7ci5L3wR&gclid=Cj0KCQjwqcO_BhDaARIsACz62vMkK3ETSnW2w7mo0Fa-wgWJGn89AxWCyIND6k5X8MmoPl6hv6VWwT8aAiS-EALw_wcB) |
| MAX17048G+T10 | [Model](https://www.snapeda.com/parts/MAX17048G+T10/Analog+Devices/view-part/?ref=eda) | [Datasheet](https://www.alldatasheet.com/view.jsp?Searchword=Max17048&gad_source=1&gbraid=0AAAAADcdDU8aYfZtfJfdZ9I5j6RwZ_cbA&gclid=Cj0KCQjwqcO_BhDaARIsACz62vNa9xrVfzjCjADRwXD0RBbo4Nret3ywwteDGLJKZui8ZL8KdVlTE7caAvQxEALw_wcB) |
| MCP73831T-5ACI/OT | [Model](https://www.mouser.co.uk/ProductDetail/Microchip-Technology/MCP73831T-5ACI-OT?qs=hH%252BOa0VZEiAcgAcEkuamXg%3D%3D) | [Datasheet](//efaidnbmnnnibpcajpcglclefindmkaj/https://ww1.microchip.com/downloads/en/DeviceDoc/MCP73831-Family-Data-Sheet-DS20001984H.pdf) |

## Functionalitate Hardware

Proiectul are la baza un circuit electronic compact, conceput pentru un dispozitiv de tip E-Book. Componentele principale sunt:

###  USB-C + Protectie ESD
- Asigura alimentarea dispozitivului.
- Se conecteaza prin interfata USB.
- Include protectie ESD pentru siguranta suplimentara.

###  SD Card
- Serveste ca mediu de stocare pentru cartile electronice.
- Functioneaza la 3.3V si comunica prin SPI cu microcontrollerul.

###  E-Paper Display + Module Asociate
- Include E-Paper Drive Circuit, Display Header si modulul EPD Power.
- Display Header se conecteaza la microcontroller prin SPI.
- EPD Power genereaza tensiunile necesare, iar Drive Circuit furnizeaza semnalele de control.
- Consum maxim la refresh: 30mA (alb-negru) / 60mA (color); consum zero in inactivitate.

### Senzor de Mediu - BME688
- Masoara temperatura, umiditate, presiune si calitatea aerului.
- Comunica prin I2C si functioneaza la 3.3V.
- Consum: <1uA in standby, 1–2mA in functionare.

### Modul RTC - DS3231SN
- Pastreaza ora si data curenta chiar si cu microcontrollerul oprit.
- Functioneaza pe baterie, cristal integrat de 32KHz.
- Comunica prin I2C.
- Consum: 150uA normal, 1uA pe baterie.

###  Memorie Flash Externa - 64MB NOR
- Extinde spatiul de stocare al microcontrollerului.
- Interfata SPI.
- Consum redus: 30–50mA la scriere/stergere, 10–20uA in standby.

###  Regulator de Tensiune LDO
- Asigura 3.3V pentru microcontroller.
- Consum foarte mic (~8uA activ), ideal pentru dispozitive pe baterii.

###  Supraveghetor de Tensiune
- Monitorizeaza stabilitatea tensiunii.
- Previne pornirea in conditii de tensiune necorespunzatoare.

###  Conector Qwiic/Stemma QT
- Permite conectarea facila a senzorilor prin I2C.
- Suporta conectarea in lant fara cabluri suplimentare.

###  Controler Baterie Li-Po
- Gestioneaza incarcarea/descarcarea bateriei.
- Previne suprasarcina si descarcarea profunda.


## Microcontroller - ESP32-C5

Platforma principala este modulul **ESP32-C5-WROOM**, un microcontroller performant cu consum redus, conectivitate moderna si suport pentru multiple interfete:

- **Consum energetic estimat:**
  - Activ: 100–120mA
  - Idle: 10–15mA
  - Deep Sleep: 10–20uA
- **Conectivitate:** Wi-Fi 6 (2.4 GHz), Bluetooth 5, USB nativ
- **Interfete:** GPIO, SPI, I2C, UART

### Conexiuni ESP32-C6

| Functie                    | Pini ESP32-C6             |
|---------------------------|---------------------------|
| Alimentare & Reset        | 3V3, GND, EN              |
| USB-C                     | GPIO13 (USB_D+), GPIO14 (USB_D-) |
| SD Card (SPI)             | GPIO27 (MISO), GPIO7 (MOSI), GPIO6 (SCK), GPIO4 (SS_SD) |
| E-Paper Display           | GPIO11 (EPD_CS), GPIO5 (EPD_DC), GPIO21 (EPD_RST), GPIO26 (EPD_BUSY) |
| Senzor BME688 (I2C)       | GPIO19 (SDA), GPIO20 (SCL), GPIO17 (I2C_PW) |
| UART                      | TXD0, RXD0                |
| Flash Extern              | FLASH_CS                  |
| Alte functii              | IO/BOOT, RTC_PWM, RTC_RST, INT_RTC |


## Design PCB & Amplasare Componente

Amplasarea componentelor pe placa a fost realizata cu grija, respectand bune practici pentru performanta si fiabilitate:

- **ESP32-C6** – pozitionat sus, cu antena orientata spre exterior si zona PCB decupata pentru semnal clar.
- **USB-C** – centrat in partea de jos, aliniat cu carcasa.
- **Display Header** – lateral, cu decupaj dedicat pentru ribbon.
- **Qwiic Connector** – pe margine, spatiu suficient pentru conectare facila.
- **Baterie** – PCB decupat pentru a acomoda dimensiunea bateriei Li-Po.
  
 ## Erori

  La editarea PCB-ului am intampinat urmatoarele erori:
  
- Smd, Copper Width - Net Class: 1 POWER
- Smd-Hole, Board Outline Clearance
 Smd-Hole, Board Outline Clearance
