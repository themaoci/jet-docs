## Explanation of Gameplay config inside server files

Location: user/configs/gameplay.json

```json
{
  "autosave": {
    "saveOnReceive": true, // should save profiles on received request
    "saveOnExit": true, // should save profiles on exiting of application
    "saveIntervalSec": 9999 // should save profiles in this intervals (numbers are seconds)
  },
  "inraid": {
    "saveLootEnabled": true, // should save profile after extraction (match end)
    "saveWeaponDurability": true, // should save weapon durability after extraction
    "saveHealthEnabled": true, // should save health after extraction
    "saveHealthMultiplier": 0.1,
    "miaOnTimerEnd": true // should set MissedInAction if timer runs out
  },
  "other": {
    "RedeemTime": 48 // how long items are hold in messages
  },
  "defaultRaidSettings": {
    // startup settings setup on entering screen
    "aiAmount": "AsOnline", // AI amount
    "aiDifficulty": "AsOnline", // Difficulty of AI
    "bossEnabled": true, // SHould boss be able to spawn on map
    "scavWars": false, // enabling kos for every bot
    "taggedAndCursed": false // should you be tagged and cursed ?
  },
  "hideout": {
    "productionTimeDivide_Areas": 100, // divide areas time by specified nomber
    "productionTimeDivide_ScavCase": 100, // divide scav case time by specified nomber
    "productionTimeDivide_Production": 100 // divide production time by specified nomber
  },
  "bots": {
    "pmc": {
      "enabled": true, // enable PMC spawns
      "usecChance": 50, // chance to spawn Bears or Usecs / 0 means all bears and 100 means all Usecs
      "types": {
        "followerTest": 100,
        "bossTest": 100,
        "assault": 35,
        "pmcBot": 35
      }
    },
    "limits": {
      "assault": 30, // how much bots to send per request
      "marksman": 30, // how much bots to send per request
      "pmcBot": 30, // how much bots to send per request
      "bossBully": 30, // how much bots to send per request
      "bossGluhar": 30, // how much bots to send per request
      "bossKilla": 30, // how much bots to send per request
      "bossKojaniy": 30, // how much bots to send per request
      "bossSanitar": 30, // how much bots to send per request
      "followerBully": 30, // how much bots to send per request
      "followerGluharAssault": 30, // how much bots to send per request
      "followerGluharScout": 30, // how much bots to send per request
      "followerGluharSecurity": 30, // how much bots to send per request
      "followerGluharSnipe": 30, // how much bots to send per request
      "followerKojaniy": 30, // how much bots to send per request
      "followerSanitar": 30, // how much bots to send per request
      "test": 30, // how much bots to send per request
      "followerTest": 30, // how much bots to send per request
      "bossTest": 30 // how much bots to send per request
    }
  },
  "trading": {
    "ragfairMultiplier": 3.5, // multiply prices in flea market by this value
    "repairMultiplier": 1, // multiply repair values by this amount
    "insureMultiplier": 0.1, // multiply insurance cost by this amount
    "insureReturnChance": 75, // chance of getting your items back
    "fenceAssortSize": 60, // how much items to spawn in fence (if less are set in assort it will spawn all)
    "buyItemsMarkedFound": true, // buy items as found in raid
    "traderSupply": {
      // supply timers update per seconds specified
      "5a7c2eca46aef81a7ca2145d": 3600,
      "5ac3b934156ae10c4430e83c": 3600,
      "5c0647fdd443bc2504c2d371": 3600,
      "54cb50c76803fa8b248b4571": 3600,
      "54cb57776803fa99248b456e": 3600,
      "579dc571d53a0658a154fbec": 600,
      "5935c25fb3acc3127c3d8cd9": 3600,
      "58330581ace78e27b8b10cee": 3600
    }
  },
  "location": {
    "realTimeEnabled": true, // count using real time
    "forceWeatherEnabled": false, // force weather specified below
    "forceWeatherId": false // choose id of weather shown in server startup :) (need to be number)
  },
  "locationloot": {
    "containers": {
      "ChanceForEmpty": 10, // chance to get empty container
      "ChanceToSpawnNextItem": 40, // chance to spawn next item in container (counting from first one) (it goes through all slots of container)
      "AttemptsToPlaceLoot": 3, // how much tries to place item that doesnt fit?
      "RarityMultipliers": {
        // not much used in other places except containers :) it jsut multiplies the chance by specified number
        "Not_exist": 0,
        "Common": 1,
        "Rare": 0.7,
        "Superrare": 0.4
      }
    },
    "useDynamicLootFromItemsArray": false, // if false using dynamic file loot assign its best chosoe otherwise will spawn items from loot spawn point which mostly are 1 item.
    "useDynamicLootMultiplier": true // increase loot spawn chance closer to 1 depending on what map you are succesfully extracted from :) mostly goes from 0.5 up to 1
  },
  "match": {
    "enabled": false // enables / disables matchmaking (should be false cause we dont have amtchmaking...)
  }
}
```
