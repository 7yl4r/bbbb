# bbbb
big blue bus build

```mermaid
graph TD

classDef todo fill:#a00

SHORE((shore power))  
BATT[(12V battery bank)]
INVERT{{MultiPlus-II inverter+switcher}}
SOLAR[[solar \n panels]]:::todo
BMS:::todo
T1{{included charger hookup 120VAC->12V}}
T2{{trickle charger 120VAC->12V}} 
LOAD120[120V Distributor]
MPPT{{MPPT}}:::todo

SHORE -.0g 0m solid copper.-> T1 -.?.->BATT
SHORE --> INVERT:::todo
SHORE --?--> T2 --?--> BATT2

BATT
  -.?.->INVERT:::todo
BATT
  -.?.->LOAD12[12V load]

BATT2[(12V Starter Batteries)]

INVERT-.?.->LOAD120

SOLAR-->MPPT-->BATT

BMS  -.?.->BATT
  
```

## useful links
* [vanlifee outfitters load calculation guide](https://www.vanlifeoutfitters.com/sizing-your-electrical-system-load-calculations/)
* [vanlife outfitters recommended parts gsheet](https://docs.google.com/spreadsheets/d/11mebU5YFH1MwnHQXBB2S3vVxYF2hY864WwTCBpQJXPs/edit#gid=0)
* [vanlife outfitters external BMS van build](https://www.vanlifeoutfitters.com/camper-van-electrical-system-with-victron-smart-batteries-and-external-bms/)
    * includes comparison of VE.BUS BMS & LYNX smart BMS
    * includes MPPT

## reference systems:
See [this bbb electrical ref gsheet](https://docs.google.com/spreadsheets/d/1SF7AyHANk0NwJzxiIKbziExU9UKyV6MDn2Jnl_4Plks/edit?usp=sharing) for links & analysis of different electrical diagrams reviewed in the process of designing the bbb electrical system
