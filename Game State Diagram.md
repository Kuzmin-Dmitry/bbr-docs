stateDiagram-v2
    direction LR
    [*] --> TitleScreen
    TitleScreen --> MainMenu
    TitleScreen --> NewPlayerTutorial : First time

    state MainMenu {
        [*] --> Idle
        Idle --> GameModes
        Idle --> CharacterSystem
        Idle --> SocialFeatures
        Idle --> Shop
        Idle --> Inventory
    }

    MainMenu --> Loading
    Loading --> GameplayState

    state GameplayState {
        [*] --> BattlePreparation
        BattlePreparation --> Combat
        Combat --> BattleResult
        BattleResult --> RewardDistribution
        RewardDistribution --> PostBattleOptions
        PostBattleOptions --> BattlePreparation : Retry
        PostBattleOptions --> [*] : Exit

        state Combat {
            [*] --> PlayerTurn
            PlayerTurn --> EnemyTurn
            EnemyTurn --> PlayerTurn
            PlayerTurn --> [*] : Battle End
            EnemyTurn --> [*] : Battle End
        }
    }

    GameplayState --> Loading
    Loading --> MainMenu

    state GameModes {
        [*] --> StoryMode
        [*] --> DailyDungeons
        [*] --> PvPArena
        [*] --> GuildHub
        StoryMode --> GameplayState
        DailyDungeons --> GameplayState
        PvPArena --> GameplayState
        GuildHub --> GameplayState
    }

    state CharacterSystem {
        [*] --> Summoning
        [*] --> CharacterManagement
        CharacterManagement --> LevelUp
        CharacterManagement --> Evolution
        CharacterManagement --> SkillUpgrade
    }

    state SocialFeatures {
        [*] --> FriendList
        [*] --> ChatSystem
        [*] --> LeaderboardsView
    }

    state Shop {
        [*] --> ItemShop
        [*] --> PremiumShop
        [*] --> SpecialOffers
    }

    state Inventory {
        [*] --> CharacterInventory
        [*] --> EquipmentInventory
        [*] --> ConsumableInventory
    }

    MainMenu --> EventsHub
    EventsHub --> GameplayState

    note right of MainMenu : Push notifications can trigger transitions to various states from here
    note right of GameplayState : Core gameplay loop occurs here, including all battle-related states
    note left of CharacterSystem : Character progression and management occurs here
    note left of Shop : In-game purchases and economy management
    note left of Inventory : Item and character management