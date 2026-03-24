# x4-controller-config
Full controller support for X4 Foundations, with preserved keyboard + mouse functionality. Based on Eillis' great work...

https://steamcommunity.com/sharedfiles/filedetails/?id=2954560643

In addition to the benefits of tracking this in source control, there are a couple of enhancements...

* Updated the inputmap version `158` -> `185` (March 2026).
* Preserve default keyboard + mouse functionality for seamless mixed use.
  * See [Steam Controller Layout Reference](./Layout-Reference-SpoddyCoder.md) for more details.
  * TODO: re-implement bindings that Eillis had to remove to make room for the modifiers.


## Usage
* Setup Steam controller support to use the `SpoddyCoder-X4-Layout` Steam Controller layout.
  * See [Eillis' guide](https://steamcommunity.com/sharedfiles/filedetails/?id=2954560643), but choose the `SpoddyCoder-X4-Layout` from the community layouts instead.
* Drag `inputmap_5.xml` into your `{YOUR_DOCUMENTS}/Egosoft/X4/{NUMBERS}/` folder.
  * If you're just the sort of person to have a 5th controller profile already, I probably don't need to tell you to take a backup before overwriting it.
* Load the 5th controller profile in-game.

### Steam Controller Layout and In-Game Bindings Reference
* Each version has a document that describes its own layout.
* `inputmap_5.xml` is the main profile, and currently tracks [versions/185_5_spoddycoder.xml](./versions/185_5_spoddycoder.md).

### Modifying
* Docs and commit history should be helpful to anyone who wants to configure Eillis' setup to their own tastes. 
* Remember to save to profile 5 as you make changes, this will serve as your backup.
* If you want to track your changes in git, see [Setup For Dev](#setup-for-dev).


## `versions/`
* [158_1_eillis.xml](./versions/158_1_eillis.md) - Eillis' original config. Uses `X4 Eilli's Gamepad` layout.
* [185_1_eillis.xml](./versions/185_1_eillis.md) - Eillis' original config updated to v185 spec. Uses `X4 Eilli's Gamepad` layout.
* [185_1_default.xml](./versions/185_1_default.md) - Latest default config shipped with the game.
* [185_2_eillis-remap.xml](./versions/185_2_eillis-remap.md) - Eillis' config, remapped to use the `SpoddyCoder-X4-Layout` Steam Controller layout.
  * Use this if you want Eillis' original scheme, but with the flexibility to rebind the controls for full keyboard + mouse functionality.
* [185_5_spoddycoder.xml](./versions/185_5_spoddycoder.md) - my config, uses the `SpoddyCoder-X4-Layout`, modded for a "FPV" drone flight style, as well as other tweaks.

NOTE: the main `inputmap_5.xml` profile currently tracks `versions/185_5_spoddycoder.xml`. If you want to use any of the other versions, see below.


## Setup For Dev
Making changes to the **in-game** `inputmap_5.xml` should be reflected directly in the checked out repo version, so we can see the diff and commit changes.

* Run `cmd` (as admin) and create a link to the config file in the game directory to wherever you've checked out the repo, eg:
* `mklink "C:\Users\{USERNAME}\Documents\Egosoft\X4\10112698\inputmap_5.xml" "C:\Users\{USERNAME}\x4-controller-config\inputmap_5.xml"`
* You can ofc use any of the versions, eg: Eilli's original but with the remapped controls:
* `mklink "C:\Users\{USERNAME}\Documents\Egosoft\X4\10112698\inputmap_2.xml" "C:\Users\{USERNAME}\x4-controller-config\versions\185_2_eillis-remap.xml"`
* Don't forget to actually save the controller profile in-game after making changes.
* Similarly, if you make changes to the file directly, you'll need to load it in-game.

### WSL dev limitations
* Getting a link between a file located on the WSL instance and a file on the windows host is problematic - the two approaches you might try both have issues...
  * Cannot simply move the repo to a windows mounted dirctory on the WSL instance - this has performance + other issues when using an IDE on the host.
  * Not sure it's possible to have the windows host application (x4) access a file on a WSL instance filesystem.
    * Even if you could - this would mean you now require the WSL instance running to use the config... not ideal.
* Recommend you just use the windows host directly for this project.


## Contributing
PR's are welcome for any changes that would benefit everyone using this config. Just fork it if it's a personal preference thing, innit.
