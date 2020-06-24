# ModUpdater
A simple Minecraft mod updater.

Created For [ModFest 1.16](https://modfest.net/1.16)

**NOTE:** This is only able to scan mods that have opted-in!

## Mod Users
Go to the Mod Menu and click the configure icon for ModUpdater.

## Mod Developers
Place this in your ``fabric.mod.json``:

**Maven**
```json
{
    "custom": {
        "modupdater": {
            "strategy": "maven",
            "repository": "https://maven.fabricmc.net",
            "group": "net.fabricmc.fabric-api",
            "artifact": "fabric-api"
        }
    }
}
```

**CurseForge**
```json
{
    "custom": {
        "modupdater": {
            "strategy": "curseforge",
            "projectID": 306612
        }
    }
}
```

**GitHub Releases**
```json
{
    "custom": {
        "modupdater": {
            "strategy": "github",
            "owner": "Repository Owner",
            "repository": "Repository Name"
        }
    }
}
```

Also replace this in ````build.gradle````:
```gradle
version = project.mod_version
```
with:
```gradle
version = "${project.mod_version}+${project.minecraft_version}"
```

## Changelog
[View Changelog](CHANGELOG.md)

## Credits
- The icon was created by ``ProspectorDev``
- The GitHub Releases strategy was written by ``AppleTheGolden``