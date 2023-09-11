# bbbb
The electrical system is designed using the "US-Van-Manual-&-Drawing-VEBus-BMS-V2-MultiPlus-II-3kVA-12V-120V-60Hz.pdf" as the primary guide.

```mermaid
graph TD

classDef todo fill:#a00

SHORE((shore power))  
BATT_BANK[(12V battery bank)]
INVERT{{MultiPlus-II \n 12V->120AC \n inverter+switcher}}
%% BMS_t2{{included charger hookup \n 120VAC->12V}}
%% BMS_t1{{trickle charger \n 120VAC->12V}} 
dist120[120V Dist Panel]
%% MPPT{{MPPT}}:::todo
%% SOLAR[[solar \n panels]]:::todo
%% BMS{{fancy BMS}}:::todo
%% BATT2[(12V Starter Batteries)]

%% SHORE -.?g ?m solid copper.-> T1 -.?.->BATT
%% SHORE --?--> T2 --?--> BATT2

SHORE -- "[50A] 2m 6g" --> F30:::todo --> INVERT:::todo
INVERT -- "[50A] 1m 6g" --> dist120:::todo

dist120 --> aircon
dist120 --> lights
dist120 --> kitchen_appliances

%% === 12V system
%% BMS  -.?.->BATT
%% BATT
%%   -.?.->INVERT:::todo
%% BATT
%%   -.?.->LOAD12[12V load]



%% SOLAR-->MPPT-->BATT
```

## useful links
* [vanlifee outfitters load calculation guide](https://www.vanlifeoutfitters.com/sizing-your-electrical-system-load-calculations/)
* [vanlife outfitters recommended parts gsheet](https://docs.google.com/spreadsheets/d/11mebU5YFH1MwnHQXBB2S3vVxYF2hY864WwTCBpQJXPs/edit#gid=0)
* [vanlife outfitters external BMS van build](https://www.vanlifeoutfitters.com/camper-van-electrical-system-with-victron-smart-batteries-and-external-bms/)
    * includes comparison of VE.BUS BMS & LYNX smart BMS
    * includes MPPT

## reference systems:
See [this bbb electrical ref gsheet](https://docs.google.com/spreadsheets/d/1SF7AyHANk0NwJzxiIKbziExU9UKyV6MDn2Jnl_4Plks/edit?usp=sharing) for links & analysis of different electrical diagrams reviewed in the process of designing the bbb electrical system
