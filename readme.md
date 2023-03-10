# website-data
This repo houses the data that is pulled by _FleetCommand.Academy_. Below are the object definitions for each file.

# Officers
```json
"officers": [
  {
    "name": string,
    "icon": string,
    "class": ("Engineering" | "Science" | "Command"),
    "group": string,
    "faction": ("Federation" | "Klingon" | "Romulan" | "Independant"),
    "description": string,
    "abilities": [
      {
        "name": string,
        "location": ("Captain" | "Officer" | "Below Deck"),
        "description": string,
        "icon": string,
        "status": {
          "name": ("Morale" | "Hull Breach" | "Assimilated" | "Burning"),
          "givesStatus": bool,
          "usesStatus": bool,
          "preventsStatus": bool
        },
      },
    ],
    "
    "notes": string,
    "introduced": string,
  }
]
```

# Officer Combinations 
```json
```

# Ships
```json
```

# Research
```json
```

# Fleet Commanders
```json
```
