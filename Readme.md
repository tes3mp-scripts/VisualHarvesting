This is a tes3mp version of graphic herbalism. Players can activate plants, removing them from the world and gaining ingredients. Whenever a cell is loaded, all the harvested plants respawn, if enough time has passed.

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