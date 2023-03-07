# Example Datapack
You can take a look at an example datapack at https://github.com/kleiders3010/skills-collection/releases

# Skills Collection works with datapacks
1. Create a pack.mcmeta by making a normal txt file and renaming it to pack.mcmeta
2. Then you will need this in your pack.mcmeta:
```
{
  "pack": {
    "description": "My datapack or whatever you want to put here",
    "pack_format": 9,
    "forge:data_pack_format": 10
  }
}
```

# Getting the information you need


modid: You'll find it by hovering an item in game and checking what's before the ":"

registrynames: When you're in-game, you can press F3+H to turn on Advanced Tooltips to see the registry name of items, here is where you see the mod id too. The registry name is after the ":"


# Addings the actual rewards to your datapack
You need to add rewards based on the main item modid

data -> {modid} -> skill_item -> {registrynames}.json

Example:
data -> botania -> skill_item -> magic_sunflower.json

data -> minecraft -> skill_item -> diamond.json



Then, inside the datapack, you need to put the rewards data.
There is 2 fields: rewards, and xp_needed, like so:
```
{
  "rewards": {
	"0": "minecraft:stick",
	"1": "minecraft:apple",
	"3": "minecraft:emerald",
	"4": "minecraft:gold_ingot",
	"6": "minecraft:emerald",
	"7": "minecraft:diamond_sword",
	"8": "minecraft:iron_ingot"
  },
  "xp_needed": {
	"0": "1",
	"1": "10",
	"3": "27",
	"4": "50",
	"6": "75",
	"7": "100",
	"8": "120"
  }
}
```
You can put from 0 to 8 rewards, and you don't need to fill in all the rewards if you don't want to; XP is gained by picking up the item, so 25xp is equal to picking up 25 of the collection item, in this example that would be botania:magic_sunflower

# Placing the datapack
You can place the datapack inside your mod like how you would put any other data, or you could place them inside your map folder or servers datapack folder!

# How it looks like in game
