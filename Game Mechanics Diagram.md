graph TD
    A[Core Gameplay] --> B[Combat System]
    A --> C[Character Collection]
    A --> D[Progression System]
    A --> E[Social Features]
    
    B --> B1[Turn-based Battles]
    B --> B2[Elemental Affinities]
    B --> B3[Skill System]
    B1 --> B1a[Speed-based Turn Order]
    B2 --> B2a[5 Elements: Fire, Water, Earth, Air, Dark]
    B3 --> B3a[Active Skills]
    B3 --> B3b[Ultimate Abilities]
    
    C --> C1[Gacha Summoning]
    C --> C2[Character Rarity]
    C2 --> C2a[Common, Rare, Epic, Legendary, Mythic]
    C1 --> C3[Character Inventory]
    
    D --> D1[Character Leveling]
    D --> D2[Evolution System]
    D --> D3[Equipment System]
    D1 --> D1a[EXP Gain]
    D2 --> D2a[Evolution Materials]
    D3 --> D3a[Weapon, Armor, Accessory]
    
    E --> E1[Guild System]
    E --> E2[PvP Arena]
    E --> E3[Friend System]
    E1 --> E1a[Guild Raids]
    E2 --> E2a[Ranked Battles]
    
    F[Resource Management] --> F1[Gold]
    F --> F2[Gems]
    F --> F3[Stamina]
    F --> F4[Evolution Materials]
    
    G[Game Modes] --> G1[Story Campaign]
    G --> G2[Daily Dungeons]
    G --> G3[Events]
    G1 --> G1a[Chapters and Stages]
    G2 --> G2a[Element-specific Dungeons]
    G3 --> G3a[Limited-time Quests]
    
    H[Monetization] --> H1[Premium Summons]
    H --> H2[Special Packs]
    H --> H3[Battle Pass]
    
    I[Engagement Systems] --> I1[Daily Login Rewards]
    I --> I2[Achievements]
    I --> I3[Quests]
    
    J[UI Systems] --> J1[Main Hub]
    J --> J2[Battle Screen]
    J --> J3[Character Management]
    
    %% Connections between systems
    B1 --> D1
    B3 --> D1
    C1 --> F2
    D1 --> F1
    D2 --> F4
    E1a --> F1
    G --> F3
    H --> F2
    I --> F