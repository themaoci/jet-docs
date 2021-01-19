# JustEmuTarkov Installation

> ***If you are having issues with the installation, review the FAQ at the bottom of this page.***

## Installation Video

<video width="720" height="480" controls>
  <source src="https://static.kiobu.dev/install.mp4">
</video>

## Requirements

- Archive unpacker (7zip, WinRAR, etc.).
- Server files (named **JET_X.X.X_Server.7z**), where **X.X.X** is the latest JET server release.
- A supported Escape from Tarkov client version. These are available below.
- Binary files that match your EFT client version (named **JET-Binaries-XXXX.7z**), where **XXXX** is your client version.

## Download Center

To download the JET server and JET binaries, the archives are hosted on [mega.nz](https://mega.nz/folder/Fg1WCAbR#LVAylusBUPB0cJ6QQXI2QA).

To download EFT clients supported by JET, you must download one of the below client archives:

- [0.12.7.9018](https://maoci.eu/download?file=EFT0.12.7.9018) *(not recommended)*
- [0.12.8.9506](https://maoci.eu/download?file=EFT0.12.8.9506)
- [0.12.8.9767](https://maoci.eu/download?file=EFT0.12.8.9767) *(latest supported version)*
  - [Alternate Mirror](https://drive.google.com/file/d/1sTOZ2AcO68pqbc9UjsZ94588ihCnB9Jp/view)

Make sure the binaries you download from the download center match the client version you download.

## Installation Process

1. Create a master folder where you want your JET-related files to be. We will call this folder `JET`. Inside, create two folders, `Client` and `Server`.

```
JET/
|
|__Server/
|
|__Client/
```

2. Extract your downloaded EFT **client files** to `JET/Client`.

3. Extract your downloaded JET **server files** to `JET/Server`.

4. Extract your downloaded JET **client binaries** to `JET/Client`. You should get a message asking if you want to overwrite existing files, select **Yes.** Your directories should now look similar to the following:

```
JET/
|
|__Server/
|  |__Server.exe
|  |__db/
|  |__res/
|  |__src/
|  |__user/
|
|__Client/
|  |__ ...
|  |__EscapeFromTarkov.exe
|  |__JET Launcher.exe
|  |__launcher.config.json
|  |__EscapeFromTarkov_Data/
|     |__Managed/
|        |__ ...
|        |__NLog.JET.dll
|        |__0Harmony.dll
|        |__Assembly-CSharp.dll
|        |__NLog.dll.nlog
```

5. You are ready to begin playing. Launch `JET/Server/Server.exe`. You should see the server print: `Server is working at: https://127.0.0.1:443`

6. Launch `JET/Client/JET Launcher.exe`. 
    - Make sure the server is running before you start the launcher.

7. If the server box says `JustEmuTarkov`, then hit **Connect** and you will be connected to your JET server.

8. To login, you can use the pre-created account with the username *Maoci* and the password *123*, or you can create your own by selecting **Create Profile**.
    - The e-mail and password do not need to be legitimate. You can enter whatever text you want into the boxes, as long as you remember them.

9. After choosing what version you want and registering, login to your new account. 

10. Press **Start Game**, and you should now be launching JET's EFT.

## Install FAQ

**Q:** *I am getting an NLog related error and it's preventing me from running the JET Launcher!*

- **A:** *Go to your `JET/Client/EscapeFromTarkov_Data/Managed/` folder. Now, look for all files related to NLog and go to their properties. At the bottom, you should see an checkbox labeled* **Unblock***. Unblock all NLog files. If this does not work, reinstall your client binaries.*
