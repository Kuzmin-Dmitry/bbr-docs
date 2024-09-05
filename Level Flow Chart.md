graph TD
    Start[Game Start] --> Tutorial[Tutorial Stages]
    Tutorial --> Chapter1[Chapter 1: The Awakening]
    
    subgraph Chapter1
        C1S1[Stage 1-1: The Summoning] --> C1S2[Stage 1-2: First Steps]
        C1S2 --> C1S3[Stage 1-3: Dark Forests]
        C1S3 --> C1S4[Stage 1-4: Ancient Ruins]
        C1S4 --> C1S5[Stage 1-5: Boss Battle]
    end
    
    Chapter1 --> Chapter2[Chapter 2: The Dark Covenant]
    
    subgraph Chapter2
        C2S1[Stage 2-1: City of Shadows] --> C2S2[Stage 2-2: Underground Passages]
        C2S2 --> C2S3[Stage 2-3: The Catacombs]
        C2S3 --> C2S4[Stage 2-4: Chamber of Rituals]
        C2S4 --> C2S5[Stage 2-5: Boss Battle]
    end
    
    Chapter2 --> Chapter3[Chapter 3: Elemental Trials]
    
    subgraph Chapter3
        C3S1[Stage 3-1: Trial of Fire] --> C3S2[Stage 3-2: Trial of Water]
        C3S2 --> C3S3[Stage 3-3: Trial of Earth]
        C3S3 --> C3S4[Stage 3-4: Trial of Air]
        C3S4 --> C3S5[Stage 3-5: Trial of Darkness]
    end
    
    Chapter3 --> MoreChapters[Chapters 4-10...]
    
    DailyDungeons[Daily Dungeons] -.-> Chapter1
    DailyDungeons -.-> Chapter2
    DailyDungeons -.-> Chapter3
    
    Events[Special Events] -.-> Chapter1
    Events -.-> Chapter2
    Events -.-> Chapter3
    
    PvPArena[PvP Arena] -.-> Chapter2
    
    GuildRaids[Guild Raids] -.-> Chapter3
    
    %% Difficulty progression
    classDef easyStage fill:#90EE90,stroke:#333,stroke-width:2px;
    classDef mediumStage fill:#FFD700,stroke:#333,stroke-width:2px;
    classDef hardStage fill:#FFA07A,stroke:#333,stroke-width:2px;
    
    class C1S1,C1S2,C1S3 easyStage;
    class C1S4,C1S5,C2S1,C2S2 mediumStage;
    class C2S3,C2S4,C2S5,C3S1,C3S2,C3S3,C3S4,C3S5 hardStage;
    
    %% Unlocking conditions
    C1S5 -->|Unlock condition: Complete all Chapter 1 stages| Chapter2
    C2S5 -->|Unlock condition: Complete all Chapter 2 stages & Player Level 10| Chapter3
    Chapter2 -->|Unlock condition: Player Level 5| PvPArena
    Chapter3 -->|Unlock condition: Player Level 15| GuildRaids