graph TD
    A[Root] --> B{Selector: Combat Role}
    B --> C{Tank Behavior}
    B --> D{Damage Dealer Behavior}
    B --> E{Support Behavior}
    
    C --> F{Sequence: Tank Actions}
    F --> G[Check Own Health]
    G --> H{Health Critical?}
    H -->|Yes| I[Use Self-Heal/Shield]
    H -->|No| J[Check Allies' Health]
    J --> K{Ally Needs Protection?}
    K -->|Yes| L[Use Taunt/Guard Skill]
    K -->|No| M[Use Basic Attack]
    
    D --> N{Sequence: Damage Dealer Actions}
    N --> O[Analyze Enemy Team]
    O --> P{Elemental Advantage?}
    P -->|Yes| Q[Target Weak Element]
    P -->|No| R[Check for Debuffed Enemy]
    R --> S{Enemy Debuffed?}
    S -->|Yes| T[Focus Debuffed Target]
    S -->|No| U[Check Ultimate Ability]
    U --> V{Ultimate Ready?}
    V -->|Yes| W[Use Ultimate on Priority Target]
    V -->|No| X[Use Strongest Single Target Attack]
    
    E --> Y{Sequence: Support Actions}
    Y --> Z[Assess Team Status]
    Z --> AA{Allies Debuffed?}
    AA -->|Yes| AB[Use Cleanse Ability]
    AA -->|No| AC[Check Ally Health]
    AC --> AD{Ally Critical Health?}
    AD -->|Yes| AE[Use Healing Skill]
    AD -->|No| AF[Check Buff Status]
    AF --> AG{Team Needs Buff?}
    AG -->|Yes| AH[Apply Team Buff]
    AG -->|No| AI[Use Basic Attack on Weakest Enemy]
    
    B --> AJ{Selector: Special Conditions}
    AJ --> AK{Boss Behavior}
    AK --> AL[Check Phase Transition]
    AL --> AM{Phase Change?}
    AM -->|Yes| AN[Trigger Special Ability]
    AM -->|No| AO[Follow Role Behavior]
    
    AJ --> AP{Minion Behavior}
    AP --> AQ[Check Summoner Health]
    AQ --> AR{Summoner in Danger?}
    AR -->|Yes| AS[Protect Summoner]
    AR -->|No| AT[Follow Role Behavior]
    
    B --> AU{Selector: Environmental Factors}
    AU --> AV[Check Battlefield Effects]
    AV --> AW{Harmful Effect Active?}
    AW -->|Yes| AX[Use Terrain Neutralizing Skill]
    AW -->|No| AY[Exploit Terrain Advantage]
    
    B --> AZ{Fallback Behavior}
    AZ --> BA[Use Basic Attack]
    
    classDef selector fill:#f9f,stroke:#333,stroke-width:2px;
    classDef sequence fill:#bbf,stroke:#333,stroke-width:2px;
    class B,AJ,AU selector;
    class F,N,Y sequence;

    %% New additions
    C --> CC[Check Threat Level]
    CC --> CD{High Threat?}
    CD -->|Yes| CE[Prioritize Defensive Skills]
    CD -->|No| CF[Balance Offense and Defense]

    D --> DG[Assess Team Composition]
    DG --> DH{Team Synergy Available?}
    DH -->|Yes| DI[Use Combo Skill]
    DH -->|No| DJ[Standard Attack Pattern]

    E --> EK[Monitor Crowd Control]
    EK --> EL{Allies Crowd Controlled?}
    EL -->|Yes| EM[Use CC Break Skill]
    EL -->|No| EN[Continue Support Routine]

    AJ --> AO{Event-Specific Behavior}
    AO --> AP[Check Event Conditions]
    AP --> AQ{Special Event Active?}
    AQ -->|Yes| AR[Use Event-Specific Skills]
    AQ -->|No| AS[Standard Behavior]