# Ebook_reader-TSC
## Prezentare generala
## Block Diagram
## Bill of Materials
https://docs.google.com/spreadsheets/d/1N5ziHIieOx6WYcnIorr_FrSW2J7KDQvOZFM7QcZUQQs/edit?gid=1760852051#gid=1760852051

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

---

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

---

## Design PCB & Amplasare Componente

Amplasarea componentelor pe placa a fost realizata cu grija, respectand bune practici pentru performanta si fiabilitate:

- **ESP32-C6** – pozitionat sus, cu antena orientata spre exterior si zona PCB decupata pentru semnal clar.
- **USB-C** – centrat in partea de jos, aliniat cu carcasa.
- **Display Header** – lateral, cu decupaj dedicat pentru ribbon.
- **Qwiic Connector** – pe margine, spatiu suficient pentru conectare facila.
- **Baterie** – PCB decupat pentru a acomoda dimensiunea bateriei Li-Po.
