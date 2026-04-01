# x4-controller-config
Full controller support for X4 Foundations. Based on Eillis' great work...

https://steamcommunity.com/sharedfiles/filedetails/?id=2954560643

Tailored for my preferences and attempted to preserve standard keyboard controls where possible for seamless dual use.


## Usage
* Setup Steam controller support to use the `SpoddyCoder-X4-Layout` Steam Controller layout.
  * See [Eillis' guide](https://steamcommunity.com/sharedfiles/filedetails/?id=2954560643), but choose the `SpoddyCoder-X4-Layout` from the community layouts instead.
* Drag `inputmap_5.xml` into your `{YOUR_DOCUMENTS}/Egosoft/X4/{NUMBERS}/` folder.
* Load the controller profile in-game.

### Steam Controller Layout and In-Game Bindings Reference
* [SpoddyCoder's Layout Reference](./docs/Layout-Reference-SpoddyCoder.md)

### Modifying
* Remember to save the profile in-game as you make changes, this will serve as your backup.
* If you want to track your changes in git, see [Setup For Dev](#setup-for-dev).


## `reference/`
* [158_eillis.xml](./reference/158_eillis.md) - Eillis' original config.
* [185_default.xml](./reference/185_default.md) - Latest default config shipped with the game.


## Setup For Dev
Making changes to the **in-game** `inputmap_5.xml` should be reflected directly in the checked out repo version, so we can see the diff and commit changes.

* Run `cmd` (as admin)
* Create a link in the game directory, pointing to the config file you want to use, wherever you've checked out the repo, eg:
  * `mklink "C:\Users\{USERNAME}\Documents\Egosoft\X4\{NUMBERS}\inputmap_5.xml" "C:\Users\{USERNAME}\x4-controller-config\versions\inputmap_5.xml"`
* Don't forget to actually save the controller profile in-game after making changes.
* Similarly, if you make changes to the file directly, you'll need to load it in-game.

### WSL dev limitations
* Getting a link between a file located on the WSL instance and a file on the windows host is problematic - the two approaches you might try both have issues...
  * Cannot simply move the repo to a windows mounted dirctory on the WSL instance - this has performance + other issues when using an IDE on the host.
  * Not sure it's possible to have the windows host application (x4) access a file on a WSL instance filesystem.
    * Even if you could - this would mean you now require the WSL instance running to use the config... not ideal.
* Recommend you just use the windows host directly for this project. Don't waste your time trying like I did...


## Contributing
PR's are welcome for any changes that would benefit everyone using this config (eg: me). Just fork it if it's a personal preference thing, innit.
