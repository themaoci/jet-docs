# Directory structure for JET server

- **db**
  - base -> contains a base files which shouldnt be changed in order to maintain consistency (advised to use TamperModLoad to edit these in memory of server)
  - bots -> contains bots and all of its data such as difficulty settings, health, inventory data, appearance, experience, names
  - customization -> contains suits and all variants of body types (head, arms, torso, legs)
  - dialogues -> not much used but it contains a respond dialogues for traders
  - hideout -> contains every data for hideout
  - items -> contains item nodes and in that item nodes there are items (consider item nodes as categories for items)
  - locales -> contains all localization for all languages (by default only 4 en/ru/fr/ge)
  - locations -> contains maps with its loot also
  - profile -> contains profiles to choose from on registry
  - quests -> contains categories/templates for items and quests
  - templates -> contains categories/templates for items and quests
  - traders -> contains all traders ingame base structure and their assortiment also with other "things"
  - weather -> weather files as json
  - version -> this file should store database compatiblility version of the game
- **res** -> contains static data such as fonts, css(style files), images, bundles
- **src** -> contains scripts avaliable for users to dig into
  - cache -> do cache of specific things in server
  - classes -> contains main classes of functions which supply data. if something is broken, its probably here.
  - callbacks(script) -> simply IMAGE/BUNDLE/DONE/NOTIFY etc. are hold inhere (we should get rid of it later on)
  - database(script) -> shows you what is loaded where from database so you can use it lateron in other scripts
  - response(script) -> holds all possible responses for server
- **user**
  - cache -> its a place where cache is stored
  - certs -> place where ssl certificates are stored
  - configs -> storage server config files such as accounts (login & passwords), gameplay, mods, server
  - events -> scheduled events to fire (most likely not used)
  - logs -> where logs are stored
  - mods -> where mods are stored (only folders from here are loaded)
  - profiles -> user created profiles
    - _{AID}_ -> specific user profile
- **Server.exe**

_Courtesy of Maoci_
