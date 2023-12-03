# NPCInvWithLinq HOW TO
### ItemData
| Property                 | Type                          | Description                                   | Example Usage                                   |
|--------------------------|-------------------------------|-----------------------------------------------|-----------------------------------------------|
| Path                     | string                        | The path of the item.                          ||
| ClassName                | string                        | The class name of the item.                    ||
| BaseName                 | string                        | The base name of the item.                     ||
| Name                     | string                        | The name of the item.                          ||
| PublicPrice              | string                        | The public price of the item.                  ||
| HeistContractJobType     | string                        | The type of the job for the Heist contract.    ||
| ToString                 | string                        | Overrides the default ToString method to represent the item.||
| ResourcePath             | string                        | The resource path of the item.                 ||
| ItemQuality              | int                           | The quality of the item.                       ||
| VeiledModCount           | int                           | The count of veiled mods.                      ||
| FracturedModCount        | int                           | The count of fractured mods.                   ||
| ItemLevel                | int                           | The item level.                                ||
| MapTier                  | int                           | The map tier of the item.                      ||
| DeliriumStacks           | int                           | The number of Delirium stacks.                 ||
| HeistContractReqJobLevel | int                           | The required job level for the Heist contract. ||
| ScourgeTier              | int                           | The Scourge tier of the item.                  ||
| Height                   | int                           | The height of the item.                        ||
| Width                    | int                           | The width of the item.                         ||
| ShieldBlockChance        | int                           | The block chance of the shield.                ||
| AttemptedPickups         | int                           | The number of attempted pickups.               ||
| InventoryId              | uint                          | The inventory ID of the item.                  ||
| Id                       | uint                          | The ID of the item.                            ||
| Distance                 | float                         | The distance of the item from the player.      ||
| IsWeapon                 | bool                          | Specifies if the item is a weapon.             ||
| IsIdentified             | bool                          | Specifies if the item is identified.           ||
| IsCorrupted              | bool                          | Specifies if the item is corrupted.            ||
| IsElder                  | bool                          | Specifies if the item is of Elder influence.   ||
| IsShaper                 | bool                          | Specifies if the item is of Shaper influence.  ||
| IsCrusader               | bool                          | Specifies if the item is of Crusader influence.||
| IsRedeemer               | bool                          | Specifies if the item is of Redeemer influence.||
| IsHunter                 | bool                          | Specifies if the item is of Hunter influence.  ||
| IsWarlord                | bool                          | Specifies if the item is of Warlord influence. ||
| IsInfluenced             | bool                          | Specifies if the item is influenced by any of the types mentioned above.||
| IsSynthesised            | bool                          | Specifies if the item is synthesized.          ||
| IsBlightMap              | bool                          | Specifies if the item is a Blight map.         ||
| IsMap                    | bool                          | Specifies if the item is a map.                ||
| IsElderGuardianMap       | bool                          | Specifies if the item is an Elder Guardian map.||
| Enchanted                | bool                          | Specifies if the item is enchanted.            ||
| AttackSpeed              | AttackSpeedData               | Gets a Weapons tooltip/LOCAL APS.     |AttackSpeed.Total >= 2.11 || AttackSpeed.Base >= 1.6|
| HasMods                  | bool                          | Checks if the item has the specified mods.     |HasMods(new string[] { "MetamorphosisItemisedBossRewards" }) // Metamorph Organ|
| ContainsString           | bool                          | returns true if any string is found in the input string, case insensitive| ContainsString(BaseName, new []{"bOOt","quiVer"})|
| ContainsStringCase       | bool                          | returns true if any string is found in the input string, case sensitive| ContainsStringCase(BaseName, new []{"Boot","Quiver"})|
| HasTag                   | bool                          | returns true if any string is found in the input string, case insensitive| HasTag(PathTags, "two_HAnd_weAPon") OR HasTag("two_HAnd_weAPon")|
| HasTagCase               | bool                          | returns true if any string is found in the input string, case sensitive| HasTag(PathTags, "two_hand_weapon") OR HasTag("two_hand_weapon")|
| HasUnorderedSocketGroup  | bool                          | returns true if a link set contains the wanted colors| HasUnorderedSocketGroup("GGBR")|
| HasSockets               | bool                          | returns true if the item has set contains the wanted colors| HasSockets("GGBR")|
| InfluenceFlags           | Influence                     | Flags representing different types of influence.||
| Rarity                   | ItemRarity                    | The rarity of the item.                        ||
| ModsNames                | List<string>                  | The list of names of the mods of the item.     ||
| PathTags                 | List<string>                  | The list of tags derived from item path.       ||
| Tags                     | List<string>                  | The list of tags from the item.                ||
| LabelOnGround            | LabelOnGround                 | The label on the ground.                       ||
| GemInfo                  | SkillGemData                  | Information about the skill gem.               ||
| AreaInfo                 | AreaData                      | Information about the current Area, only populated by devs ona  plugin by plugin basis.               ||
| StackInfo                | StackData                     | Information about the stack.                   ||
| Entity                   | Entity                        | The entity of the item.                        ||
| SocketInfo               | SocketData                    | Information about the sockets.                 ||
| ChargeInfo               | ChargesData                   | Information about the charges.                 ||
| FlaskInfo                | FlaskData                     | Information about the flask.                   ||
| AttributeRequirements    | AttributeRequirementsData     | Information about the attribute requirements.  ||
| ArmourInfo               | ArmourData                    | Information about the armor.                   |PlayerInfo.Level > 30|
| PlayerInfo               | PlayerData                    | Information about the player.                    ||
| ModsInfo                 | ModsData                      | Information about the mods.                    ||
| LocalStats               | Dictionary<GameStat, int>     | The local stats of the item.              ||
| FindMods                 | List<ItemMod>                 | Finds the mods of the specified type.          ||
| ModStats                 | IReadOnlyDictionary<GameStat, int> | Provides the summarized statistics of the mods.   |ModStats("ChaosResistImplicitBoots", "xddchatting")[GameStat.BaseChaosDamageResistancePct]>0|
| ItemStats                | IReadOnlyDictionary<GameStat, int> | Provides the summarized statistics of the item.  |ItemStats[GameStat.BaseMovementVelocityPct]>=10 // 10% ms|
| ModWeightedStatSum       | IReadOnlyDictionary<GameStat, float> | Provides the weighted summarized statistics of the mods. ||
| SumModStats              | IReadOnlyDictionary<GameStat, int> | Summarizes the statistics of the mods.            ||
| SumModStats              | IReadOnlyDictionary<GameStat, float> | Summarizes the statistics of the mods with weights. ||

### PlayerInfo

| Property     | Type                | Description                       |
|--------------|---------------------|-----------------------------------|
| Level        | int                 | Players Level.       |
| Strength		   | int              | Players Strength.|
| Dexterity		   | int              | Players Dexterity.|
| Intelligence		| int              | Players Intelligence.|

### AttackSpeed

| Property     | Type                | Description                       |
|--------------|---------------------|-----------------------------------|
| Base        | decimal                 | Base APS without additions.       |
| Total		   | decimal              | Total APS with additions.|

### AreaInfo

| Property     | Type                | Description                       |
|--------------|---------------------|-----------------------------------|
| Level        | int                 | Areas Level.       |
| Name		   | string              | Areas Name.|
| Act		   | int              | Areas Act.|
| IsEndGame		| bool              | Is Area End Game.|

### GemInfo

| Property     | Type                | Description                       |
|--------------|---------------------|-----------------------------------|
| Level        | int                 | The level of the skill gem.       |
| MaxLevel     | int                 | The maximum level of the skill gem.|
| QualityType  | SkillGemQualityTypeE | The type of quality for the skill gem.|

### StackInfo

| Property     | Type  | Description             |
|--------------|-------|-------------------------|
| Count        | int   | The count of the stack.  |
| MaxCount     | int   | The maximum stack count. |

### StackInfo

| Property | Type | Description                       |
|----------|------|-----------------------------------|
| Current  | int  | The current charge count.         |
| Max      | int  | The maximum charge count.         |
| PerUse   | int  | The charge count per use.         |

### SocketInfo

| Property        | Type                      | Description                         |
|-----------------|---------------------------|-------------------------------------|
| LargestLinkSize | int                       | The size of the largest link.       |
| SocketNumber    | int                       | The number of sockets.              |
| Links           | IReadOnlyCollection<int>   | The collection of links.            |
| SocketGroups    | IReadOnlyCollection<string>| The collection of socket groups.    |

### FlaskInfo

| Property     | Type                         | Description                           |
|--------------|------------------------------|---------------------------------------|
| LifeRecovery | int                          | The life recovery value.               |
| ManaRecovery | int                          | The mana recovery value.               |
| Stats        | Dictionary<GameStat, int>    | The dictionary of game statistics.     |

### AttributeRequirementsInfo

| Property  | Type | Description               |
|-----------|------|---------------------------|
| Strength  | int  | The strength requirement.  |
| Dexterity | int  | The dexterity requirement. |
| Intelligence | int | The intelligence requirement. |

### ArmourInfo

| Property | Type | Description              |
|----------|------|--------------------------|
| Armour   | int  | The armor value.         |
| Evasion  | int  | The evasion value.       |
| ES       | int  | The energy shield value. |
