# x4-controller-config
Full controller support for X4 Foundations, with preserved keyboard + mouse functionality. Based on Eillis' great work: [Steam Workshop Page](https://steamcommunity.com/sharedfiles/filedetails/?id=2954560643)

In addition to the benefits of treating this like code in source control, there are a couple of enhancements...

* Updated the inputmap version `158` -> `185` (March 2026).
  * [Merged with latest default config](https://github.com/SpoddyCoder/x4-controller-config/commit/3e03cf9bc047056156bb7be228fa6206fdf14346) to capture game updates to control bindings since 2023.
  * See [changelog](./CHANGELOG.md).
* Preserve default keyboard + mouse functionality for seamless mixed use.
  * See [Modified Steam Controller Layout](#modified-steam-controller-layout-spoddycoder-x4-layout) for more details.


## Usage
* Setup Steam controller support to use the `SpoddyCoder-X4-Layout` Steam Controller layout.
  * See [Eillis' guide](https://steamcommunity.com/sharedfiles/filedetails/?id=2954560643), but choose the `SpoddyCoder-X4-Layout` from the community layouts instead.
* Drag `inputmap_5.xml` into your `<Your documents>/Egosoft/X4/<numbers>/` folder.
  * If you're just the sort of person to have a 5th controller profile already, I probably don't need to tell you to take a backup before overwriting it.
* Load the 5th controller profile in-game.

### Modifying
* Docs and commit history should be helpful to anyone who wants to configure Eillis' setup to their own tastes. 
* Remember to save to profile 5 as you make changes, this will serve as your backup.
* If you want to track your changes in git, see [Setup For Dev](#setup-for-dev).

## `versions/`
* [158_1_eillis.xml](./versions/docs/158_1_eillis.md) - Eillis' original config.
* [185_1_default.xml](./versions/docs/185_1_default.md) - latest default config shipped with the game.
* [185_5_default-eillis.xml](./versions/docs/185_5_default_eillis.md) - latest default config merged with Eillis' config. `v185` spec, 5th profile slot.
* [185_5_default-eillis-remap.xml](./versions/docs/185_5_default-eillis-remap.md) - latest default config merged with Eillis' config, remapped to use the `SpoddyCoder-X4-Layout` Steam Controller layout.
* [185_4_spoddycoder.xml](./versions/docs/185_4_spoddycoder.md) - my config, uses the `SpoddyCoder-X4-Layout`, modded for a "FPV" drone flight style.

NOTE: the main `inputmap_5.xml` profile currently tracks `versions/185_5_default-eillis-remap.xml`. If you want to to use mine or any of the other versions, see below.


## Setup For Dev
Making changes to the **in-game** `inputmap_5.xml` should be reflected directly in the checked out repo version, so we can see the diff and commit changes.

* Run `cmd` (as admin) and create a link to the config file in the game directory to wherever you've checked out the repo, eg:
* `mklink "C:\Users\{USERNAME}\Documents\Egosoft\X4\10112698\inputmap_5.xml" "C:\Users\{USERNAME}\x4-controller-config\inputmap_5.xml"`
* You can ofc use any of the versions, such as mine. eg:
* `mklink "C:\Users\{USERNAME}\Documents\Egosoft\X4\10112698\inputmap_4.xml" "C:\Users\{USERNAME}\x4-controller-config\versions\185_4_spoddycoder.xml"`
* Don't forget to actually save the controller profile in-game after making changes.
* Similarly, if you make changes to the file directly, you'll need to load it in-game.


### WSL dev limitations
* Getting a link between a file located on the WSL instance and a file on the windows host is problematic - the two approaches you might try both have issues...
  * Cannot simply move the repo to a windows mounted dirctory on the WSL instance - this has performance + other issues when using an IDE on the host.
  * Not sure it's possible to have the windows host application (x4) access a file on a WSL instance filesystem.
    * Even if you could - this would mean you now require the WSL instance running to use the config... not ideal.
* Recommend you just use the windows host directly for this project.


## Modified Steam Controller Layout: `SpoddyCoder-X4-Layout`
* NOTE: this applies to the main [inputmap_5.xml](./inputmap_5.xml) profile, as well as the [spoddycoder](./versions/docs/185_4_spoddycoder.md) & [default-ellis-remap](./versions/docs/185_5_default-eillis-remap.md) versions
  * To benefit from the v185 update but still use Eillis' original steam controller layout, use the [185_5_default-ellis](./versions/docs/185_5_default-eillis.md) version.
  * TODO: reinstate all the default controls that Eillis had to remove to make room for the modifiers.
* To preserve standard keyboard controls, we need to use different modifiers keys. My steam controller layout can be found in the community setups.
* It remaps Eillis' orginals to use new unused keys...
* W -> ;
  * `INPUT_KEYCODE_W` -> `INPUT_KEYCODE_SEMICOLON`
  * `INPUT_KEYCODE_W_SHIFT` -> `INPUT_KEYCODE_SEMICOLON_SHIFT`
  * `INPUT_KEYCODE_W_CONTROL` -> `INPUT_KEYCODE_SEMICOLON_CONTROL`
* S -> '
  * `INPUT_KEYCODE_S` -> `INPUT_KEYCODE_APOSTROPHE`
  * `INPUT_KEYCODE_S_SHIFT` -> `INPUT_KEYCODE_APOSTROPHE_SHIFT`
  * `INPUT_KEYCODE_S_CONTROL` -> `INPUT_KEYCODE_APOSTROPHE_CONTROL`
* Z -> [
  * `INPUT_KEYCODE_Z` -> `INPUT_KEYCODE_LBRACKET`
  * `INPUT_KEYCODE_Z_SHIFT` -> `INPUT_KEYCODE_LBRACKET_SHIFT`
  * `INPUT_KEYCODE_Z_CONTROL` -> `INPUT_KEYCODE_LBRACKET_CONTROL`
* U -> ]
  * `INPUT_KEYCODE_U` -> `INPUT_KEYCODE_RBRACKET`
  * `INPUT_KEYCODE_U_SHIFT` -> `INPUT_KEYCODE_RBRACKET_SHIFT`
  * `INPUT_KEYCODE_U_CONTROL` -> `INPUT_KEYCODE_RBRACKET_CONTROL`
* C -> \
  * `INPUT_KEYCODE_C` -> `INPUT_KEYCODE_OEM_102`
  * `INPUT_KEYCODE_C_SHIFT` -> `INPUT_KEYCODE_OEM_102_SHIFT`
  * `INPUT_KEYCODE_C_CONTROL` -> `INPUT_KEYCODE_OEM_102_CONTROL`
* N -> /
  * `INPUT_KEYCODE_N` -> `INPUT_KEYCODE_SLASH`
  * `INPUT_KEYCODE_N_SHIFT` -> `INPUT_KEYCODE_SLASH_SHIFT`
  * `INPUT_KEYCODDE_N_CONTROL` -> `INPUT_KEYCODE_SLASH_CONTROL`
* L -> ,
  * `INPUT_KEYCODE_L` -> `INPUT_KEYCODE_COMMA`
  * `INPUT_KEYCODE_L_SHIFT` -> `INPUT_KEYCODE_COMMA_SHIFT`
  * `INPUT_KEYCODE_L_CONTROL` -> `INPUT_KEYCODE_COMMA_CONTROL`
* R -> .
  * `INPUT_KEYCODE_R` -> `INPUT_KEYCODE_PERIOD`
  * `INPUT_KEYCODE_R_SHIFT` -> `INPUT_KEYCODE_PERIOD_SHIFT`
  * `INPUT_KEYCODE_R_CONTROL` -> `INPUT_KEYCODE_PERIOD_CONTROL`


## Contributing
PR's are welcome for any changes that would benefit everyone using this config. Just fork it if it's a personal preference thing, innit.

