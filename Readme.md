This is a tes3mp version of graphic herbalism. Players can activate plants, removing them from the world and gaining ingredients. Whenever a cell is loaded, all the harvested plants respawn, if enough time has passed.

Requires [DataManager](https://github.com/tes3mp-scripts/DataManager)!

You can find the configuration file in `data/custom/__config_VisualHarvesting.json`.
* `alchemyDeterminesChance` default value is `true`. Determines, whether the amount of ingredients gathered depends purely on chance, or also on the player's alchemy skill.
* `menuId` should only be changed if another script is using the same `menuId`
* `respawnTime` how much time (in game hours) should pass until a plant grows again. By default is set to 720 = 24*30, same as vanilla Morrowind
* `fail`
  * `message` shown when player fails to gather anything
  * `sound` plays when player fails to gather anything
* `success`
  * `message` shown when player gathers anything
  * `sound` plays when player gathers anything
* `"plants"` data on what ingredients you can gather from various plants. You can find the syntax below:
```
"<container refId>": {
    "ingredient": "<ingredient refId>",
    "amount": {
        "0": <highest roll that gives 0 ingredients>",
        "1": <highest roll that gives 1 ingredients>",
        ...
    }
}
```
A plant may contain more than one ingredient.  To do so, substitute the `ingredient` string with a table of strings called `ingredients` as seen below:
```
"<container refId>": {
    "ingredients": {
        "<ingredient refId>",
        "<ingredient refId>"
    },
    "amount": {
        "0": <highest roll that gives 0 ingredients>",
        "1": <highest roll that gives 1 ingredients>",
        ...
    }
}
```
When successfully harvested, one of the listed ingredients is randomly selected and placed in the player's inventory.

### Mod Support

You can find a config file with all plants from [Province Cyrodiil](https://www.nexusmods.com/morrowind/mods/44922), [Skyrim Home of the Nords](https://www.nexusmods.com/morrowind/mods/44921), and [Tamriel Rebuilt](https://www.tamriel-rebuilt.org/downloads/main-release) at [this link](https://git.modding-openmw.com/TES3MP/tes3mp-CoreScripts/raw/branch/0.7.0-momw-modded/data/custom/__config_VisualHarvesting.json).  Simply place this version of the VisualHarvesting config file into your `data/custom/` folder, or copy the `plants` table out and adjust to suit your needs.
