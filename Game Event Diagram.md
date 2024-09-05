graph TD
    A[Game Events] --> B[Time-based Events]
    A --> C[Player-triggered Events]
    A --> D[System Events]
    
    B --> B1[Daily Reset]
    B --> B2[Weekly Reset]
    B --> B3[Seasonal Events]
    B1 --> B1a[Refresh Daily Quests]
    B1 --> B1b[Reset Dungeon Entries]
    B2 --> B2a[Reset Weekly Rewards]
    B2 --> B2b[Update PvP Rankings]
    B3 --> B3a[Holiday Events]
    B3 --> B3b[Themed Gacha Banners]
    
    C --> C1[Level Up]
    C --> C2[Character Evolution]
    C --> C3[Guild Activities]
    C1 --> C1a[Unlock New Features]
    C1 --> C1b[Reward Energy Refill]
    C2 --> C2a[Trigger Evolution Animation]
    C2 --> C2b[Update Character Stats]
    C3 --> C3a[Start Guild Raid]
    C3 --> C3b[Donate Resources]
    
    D --> D1[Push Notifications]
    D --> D2[Achievement Unlocks]
    D --> D3[Server Maintenance]
    D1 --> D1a[Energy Full Notification]
    D1 --> D1b[Event Start Notification]
    D2 --> D2a[Reward Distribution]
    D2 --> D2b[Update Player Profile]
    D3 --> D3a[Server Downtime]
    D3 --> D3b[Update Game Content]
    
    E[Event Interactions] --> E1[Event Start]
    E --> E2[Event Progress]
    E --> E3[Event Completion]
    E1 --> E1a[Update UI]
    E1 --> E1b[Add Event Quests]
    E2 --> E2a[Track Player Progress]
    E2 --> E2b[Unlock Milestone Rewards]
    E3 --> E3a[Distribute Final Rewards]
    E3 --> E3b[Update Leaderboards]
    
    F[Combat Events] --> F1[Battle Start]
    F --> F2[Turn Resolution]
    F --> F3[Battle End]
    F1 --> F1a[Initialize Battle State]
    F1 --> F1b[Apply Pre-battle Buffs]
    F2 --> F2a[Process Actions]
    F2 --> F2b[Update Turn Order]
    F3 --> F3a[Calculate Rewards]
    F3 --> F3b[Update Character EXP]
    
    G[Economic Events] --> G1[Resource Gain]
    G --> G2[Resource Spend]
    G1 --> G1a[Update Currency UI]
    G1 --> G1b[Trigger Reward Animation]
    G2 --> G2a[Validate Transaction]
    G2 --> G2b[Update Inventory]
    
    %% Event triggers and effects
    B1 --> D1
    B3 --> E1
    C1 --> D2
    C3 --> F1
    D3 --> A
    E3 --> G1
    F3 --> G1
    G2 --> C2