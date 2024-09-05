flowchart LR
    A[Start Game] --> B[Main Menu]
    B --> C{Player Action}
    
    C --> D[Story Campaign]
    D --> D1[Select Chapter/Stage] --> H
    
    C --> E[Daily Dungeons]
    E --> E1[Select Element/Difficulty] --> H
    
    C --> F[PvP Arena]
    F --> F1[Ranked/Casual Match] --> H
    
    C --> G[Guild Activities]
    G --> G1[Raid/War/Donation] --> H
    
    H[Team Selection] --> I[Battle Preparation] --> J[Combat]
    J --> K{Battle Outcome}
    K -->|Win| L[Victory Screen]
    K -->|Lose| M[Defeat Screen]
    
    L --> N[Reward Distribution]
    N --> O[EXP/Items/Currency]
    
    M --> R[Retry Option]
    R -->|Yes| I
    R -->|No| S[Return to Menu]
    
    O --> T[Inventory Management]
    T --> U[Character Upgrade]
    U --> U1[Level Up/Evolution/Skills]
    
    T --> V[Equipment Management]
    V --> V1[Equip/Upgrade Items]
    
    C --> W[Summoning]
    W --> W1[Regular/Premium] --> X[New Character]
    X --> T
    
    C --> Y[Shop]
    Y --> Y1[Purchase Items/Currency] --> T
    
    C --> Z[Events]
    Z --> Z1[Special Dungeons/Quests] --> H
    
    C --> AA[Social Features]
    AA --> AA1[Friends/Chat/Leaderboards]
    
    C --> AB[Daily Login]
    AB --> AC[Claim Rewards] --> T
    
    C --> AD[Quests]
    AD --> AD1[Daily/Weekly/Achievements]
    AD1 --> AE[Complete Quest] --> N
    
    C --> AF[Tutorial]
    AF --> AF1[Guided Missions] --> H
    
    AG[Time-gated Content]
    AG --> AG1[Energy/Shop Refresh] --> C
    
    AH[Push Notifications]
    AH --> AH1[Energy/Events/Guild] -.-> A
    
    AI[Seasonal Content]
    AI --> AI1[Battle Pass/Ranked Season] --> C
    
    S & U1 & V1 & AA1 --> C
    
    subgraph Core Gameplay Loop
        H
        I
        J
        K
        L
        M
        N
        O
        R
    end
    
    subgraph Progression Systems
        T
        U
        V
        W
        X
    end
    
    subgraph Engagement Features
        Y
        Z
        AA
        AB
        AD
        AF
        AG
        AH
        AI
    end

    %% New additions
    J --> J1[Turn-based Combat]
    J1 --> J2[Player Turn]
    J1 --> J3[Enemy Turn]
    J2 --> J4[Select Action]
    J4 --> J5[Execute Action]
    J5 --> J3
    J3 --> J6[Enemy AI Decision]
    J6 --> J7[Execute Enemy Action]
    J7 --> J2

    U1 --> U2[Skill Tree Navigation]
    U2 --> U3[Unlock New Abilities]

    W1 --> W2[Gacha Animation]
    W2 --> W3[Reveal New Character]

    Z1 --> Z2[Event Story Scenes]
    Z2 --> Z3[Event-specific Battles]

    AI1 --> AI2[Daily/Weekly Missions]
    AI2 --> AI3[Season Rewards]