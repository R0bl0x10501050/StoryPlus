# StoryPlus - The Easy Story Module

Thanks for using Story+! You now have access to over 15 different commands, all suited to help **you** create your **very own story game**!

## Setup

```lua
local StoryPlus = require(AssetID)
```

## Documentation

### Initalize

#### `StoryPlus:Setup(darkMode, typewriter)`
`darkMode`
- Type: `boolean`
- Desc: Determines if the guis will be in darkMode. True for dark mode, false for light mode. Default is light mode.

`typewriter`
- Type: `boolean`
- Desc: Determines if the text will have the typewriter effect. True for typewriter effect, false for no typewriter effect. Default is typewriter effect.

### Dialogues

#### `StoryPlus.NewDialog(msg, plr, typewriter, darkmode)`
`msg`
- Type: `string`
- Desc: What the dialogue will be

`plr`
- Type: `string`, `integer`, `Instance: Player or Model`
- Desc: The player whose thumbnail will show up as talking. Can either be a string PlayerName, int UserId, Instance player, or Instance model (for NPCs). If nil, this is set to a random player (usual practice).

`typewriter`
- Type: `boolean`
- Desc: If true, the typewriter effect will run. If false, the typewriter effect will **not** run. The default is set to **the SetUp command's value**.

`darkMode`
- Type: `boolean`
- Desc: Determines if the guis will be in darkMode. True for dark mode, false for light mode. Default is the setup's mode.

#### `StoryPlus.HideDialog()`

#### `StoryPlus.NewCountdown(Time, EndTime)`
`time`
- Type: `integer`
- Desc: The time at which the countdown starts at.

`EndTime`
- Type: `integer`
- Desc: The time at which the countdown purposely ends. Default is 0.

#### `StoryPlus.StopCountdown()`

### Player Interaction

#### `StoryPlus.CreateTool(model, name)`
`model`
- Type: `Instance`
- Desc: The instance that becomes a tool that a single player can use to do something within the game.

`name`
- Type: `string`
- Desc: The name of the tool. Useful for fetching the name of the player who picked up the tool.

#### `StoryPlus.UnlockTool(name)`
`name`
- Type: `string`
- Desc: The name of the tool. Since tools cannot be picked up immediately by a player, this method lets players click the tool to see who gets it.

#### `StoryPlus.CreateSeat(model, name)`
`model`
- Type: `Instance`
- Desc: Similar to tool, tihs is the instance that becomes a seat that a single player can sit on to do something within the game.

`name`
- Type: `string`
- Desc: The name of the seat. Useful for fetching the name of the player who sat on the seat.

#### `StoryPlus.UnlockSeat(name)`
`name`
- Type: `string`
- Desc: The name of the seat. Since seats cannot be sat on immediately by a player, this method lets players sit on the seat to see who gets to sit on it. (I'm getting tongue-tied reading this lol)
