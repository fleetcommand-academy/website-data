# website-data
This repo houses the data that is pulled by _FleetCommand.Academy_. Below are the object definitions for each file.

# Officers
```ts
type AbilityType = "Critical Chance" | "" //TODO
type OfficerGroup = "" //TODO

interface Ability {
  name: string;
  location: ("Captain" | "Officer" | "Below Deck");
  description: string;
  icon: string;
  status: {
    name: ("Morale" | "Hull Breach" | "Assimilated" | "Burning");
    effect: ("Gives" | "Uses" | "Prevents" | "Exploits")
  };
  abilityType: AbilityType
}

interface Officer {
  name: string;
  icon: string;
  class: ("Engineering" | "Science" | "Command");
  group: OfficerGroup;
  faction: ("Federation" | "Klingon" | "Romulan" | "Independent"),
  description: string;
  abilities: [Ability, Ability, Ability]
  notes: string;
  stfcSpaceLink: string;
  introduced: string;
}
```

# Officer Combinations 
```ts
type Hostile = "General" | "Eclipse" //TODO
type Ship = "Interceptor" | "Explorer" | "Battleship"

interface OfficerCombination {
  name: string;
  captain: {
    officer: Officer;
    rank: number;
  };
  firstOfficer: {
    officer: Officer;
    rank: number;
  };
  secondOfficer: {
    officer: Officer;
    rank: number;
  };
  purpose: string;
  hostileType: Hostile;
  ship: Ship;
  tags: Array[string];
  credit: string
}
```

# Ships
```ts
interface ShipAbility {

}

interface ShipRefit {

}

interface ShipProjectile {

}

interface BPSource {

}

interface Ship {
  name: string
  blueprintSources: BPSource[];

}
```

# Research
```ts
interface ResearchItem {
  name: string;
  description: string;
  isPrime: bool
  row: number;
  column: number;
  stfcSpaceLink: string;

}

interface ResearchTree {
  name: string;
  researchItems: ResearchItem[]

}
```

# Fleet Commanders
```ts
interface SkillItem {
  name: string;
  description: string;
  isTalent: bool;
  row: number;
  column: number;
}

interface SkillTree {
  name: string;
  description: string;
  skills: SkillItem[]
}

interface FleetCommander {
  name: string;
  skillTree: [SkillTree, SkillTree, SkillTree];
}
```

# Buildings
```ts
interface BuildingBonus {
  name: string;
  description: string;
}

interface Building {
  name: string;
  description: string;
  bonuses
}
```

# Inventory
```ts
interface InventoryItem {
  name: string;
  description: string;
  category: string;
  

}

interface InventoryTab {
  name: string;
  items: InventoryItem[];
}
```
