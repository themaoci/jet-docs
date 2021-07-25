## Server side mods.

_server side mods are divided in 3 parts Tamper, Cache, Ressource_

- Tamper mods are "tampering" the data already loaded into the server
- Cache mods are editing already cached data in user/cache folder in the server
- Ressource are simple mods that adds additional ressources into the server like images, or bundles (its simply require a key res inside of mod config file)

#### TypeOfModLoading

```
CacheModLoad
TamperModLoad
```

#### Example of file structure

```
-| YourModFolderName_Version
--\
---|> src
---|\
---| |> script.js
---|
---|> mod.config.json
---|> readme.md
```

#### Example of mod.config.json

```json
{
  "name": "YourModName",
  "author": "YourNickname",
  "version": "1.0.0",
  "src": {
    "src/script.js": "TypeOfModLoading"
  },
  "required": []
}
```

#### Example of: "exacly that version" of the mod is required

```json
...
"required": [
    {"name": "RequiredModName", "ver": "1.0.1"}
]
...
```

#### Example of: that version or newer of the mod is required

```json
...
"required": [
    {"name": "RequiredModName", "ver": "^1.0.1"}
]
...
```

#### Example of: script.js - which is loaded automatically after you specify it in mod.config.json

```js
exports.mod = (mod_info) => {
  /// do your code here ///
};
```

_"LOAD THIS FILE AS TypeOfModLoading"_

```js
{
    "src/script.js": "TypeOfModLoading"
}
```

#### Usage of Required mods loading feature

This feature postpone laoding of mods to later queue so you can load base mods that edits the same things to be launched first and then override that data using your mod.

### Usefull functions accesable from mod script

_`fileIO.typeNameOfFunctionHere(pass some parameters here)`_

- stringify(data, oneLiner) // oneLiner[default: false]
- createReadStream(filePath) // works same as fs.createReadStream(filePath)
- createWriteStream(filePath) // works same as fs.createWriteStream(filePath, {flags: 'w'})
- readParsed(filePath) // works same as JSON.parse(fs.readFileSync(file, 'utf8'))
- parse(string) // works same as JSON.parse(string)
- read(file) // works same as fs.readFileSync(file, 'utf8')
- exist(file) // works same as fs.existsSync(file)
- readDir(path) // works same as fs.readdirSync(path)
- statSync(path) // works same as fs.statSync(path)
- lstatSync(path) // works same as fs.lstatSync(path)
- unlink(path) // works same as fs.unlinkSync(path)
- rmDir(path) // works same as fs.rmdirSync(path)
- mkDir(path) // works same as fs.mkdirSync(path)
- write(filePath, data, raw, atomic) // raw[default: false], atomic[default:true]

logging can be done in 2 ways:

1. using internal logger:

- logger.logError(text);
- logger.logWarning(text);
- logger.logSuccess(text);
- logger.logDebug(text);
- logger.logInfo(text);
- logger.logRequest(text, data); // data[default: ""]
- logger.logData(data);
- logger.throwErr(message, where, additional) // additional[default: ""] -> throws application error like exception

2. using console.log:

- console.log(unparsedDataHere);

#### Additional

If you will need additional functionality fromk mod loading feature make sure to propose it for us so we can rethink it with you and propably add to the enxt build.
