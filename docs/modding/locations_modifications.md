## Locations - modding

you can find locations data in a few places

- Cached: user\cache\locations.json -> which contains all locations compressed for server usage, you can use CacheModLoad to intercept this code once its cached (it will be executed only once)
- DB: db\locations
  - which are splitted by Base data line waves spawnpoints name and other small looking data, and loot whic hcontains all loot spawn locations in certain maps
  - you can also find there a file named: dynamicLootAutoSpawnDetector.json whic hcontains loose loot (dynamic loot) table which tells the server what to spawn in certain locations
  - in settings user\configs\gameplay.json you can find variable named "useDynamicLootFromItemsArray" if its set to false the file from point above will be used if its set to true then server will use items saved in each location loot table in Items variable (which by default will spawn like 1 item)
