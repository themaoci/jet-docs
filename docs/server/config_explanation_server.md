## Explanation of server config file

```json
{
  "ip": "127.0.0.1", // internal IP to setup server
  "ip_backend": "127.0.0.1", // external IP for people connected to your server
  "port": 443, // port used by server
  "eventPollIntervalSec": 60, // time interval to update events
  "rebuildCache": false, // should i force rebuilding cache ?
  "name": "JustEmuTarkov", // not used anywhere
  "offline": {
    // offline mods that will be loaded (they are not always in the dll cause there is possibility that we dont need them anymore so they can be permamently disabled in dll)
    "OfflineLootPatch": true,
    "InsuranceScreenPatch": true,
    "BossSpawnChancePatch": true,
    "BotTemplateLimitPatch": true,
    "RemoveUsedBotProfilePatch": true,
    "OfflineSaveProfilePatch": true,
    "OfflineSpawnPointPatch": true,
    "WeaponDurabilityPatch": true,
    "SingleModeJamPatch": true,
    "ExperienceGainPatch": true,
    "MainMenuControllerPatch": true,
    "PlayerPatch": true,
    "MatchmakerOfflineRaidPatch": true,
    "MatchMakerSelectionLocationScreenPatch": true,
    "GetNewBotTemplatesPatch": true,
    "SpawnPmcPatch": true,
    "CoreDifficultyPatch": true,
    "BotDifficultyPatch": true,
    "OnDeadPatch": true,
    "OnShellEjectEventPatch": true,
    "BotStationaryWeaponPatch": true,
    "BeaconPatch": true,
    "DogtagPatch": true,
    "LoadOfflineRaidScreenPatch": true,
    "ScavPrefabLoadPatch": true,
    "ScavProfileLoadPatch": true,
    "ScavSpawnPointPatch": false,
    "ScavExfilPatch": true,
    "EndByTimerPatch": true,
    "SpawnRandomizationPatch": true,
    "RemoveAddOfferButton": true,
    "NoFiltersPatch": false,
    "JetLogger": true
  },
  "lootDebug": false, // should display you how much items containers and everything spawne don map?
  "hideInfoLogs": true, // should hide [INFO] logs from console ?
  "debugTimer": false, // display timer in seconds from server start (msotly used for debugging or benchmarking)
  "translations": {
    // some translation strings...
    "alreadyInUse": "The nickname is already in use",
    "tooShort": "The nickname is too short"
  }
}
```
