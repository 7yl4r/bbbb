# bbbb
big blue bus build

```mermaid
graph TD

classDef todo fill:#a00

SHORE((shore power))  
SHORE -.0g 0m solid copper.-> T1{{120VAC->12V}} -.?.->BATT
SHORE --> SWITCH:::todo
SHORE --?--> T2{{120VAC->12V}} --?--> BATT2

BATT[(12V battery bank)]
BATT-.?.->INVERT:::todo
BATT-.?.->LOAD12[12V load]

BATT2[(12V Starter Batteries)]

INVERT{{12V->120VAC}}
INVERT.->SWITCH{{?}}.->LOAD120[120V load]

SOLAR[[solar \n panels]]:::todo
SOLAR-->MPPT{{MPPT}}:::todo-->BATT
```

This system is essentially the suggested system [here](https://www.vanlifeoutfitters.com/store/discounted-victron-energy-bundle/).
