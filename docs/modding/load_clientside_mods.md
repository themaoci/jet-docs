## Client side mods.

Inside your Client game files you will see new folders you didnt saw in official game, which is "ClientMods"

inside of that folder you will see structure as follows

ClientMods

- ExternalLibraries
- \*.launch

where:
ExternalLibraries -> is folder where you store your "mods" dll's
\*.launch -> is a file named whatever you want which stores your mod name and launching function

#### Example of \*.launch

filename: JET.launch

```
ExternalLibraries\JET-SinglePlayer.dll
SinglePlayer.Initialize
```

_Info: you can also change external libraries folder name to whatever you want you jsut need to specify it in this file :)_

#### Example of c# code of method to load it without problems

```cs
public class SinglePlayer
{
    public static void Initialize()
	{
        // this will be executed !!!
    }
}
```

_Info: you can also wrap it around the namespace it really doesn't matter, will be still loaded._
