# x4-controller-config
Full controller support for X4 Foundations, with preserved keyboard + mouse functionality. Based on Eillis' great work: [Steam Workshop Page](https://steamcommunity.com/sharedfiles/filedetails/?id=2954560643)

In addition to the benefits of treating this like code in source control, there are a couple of enhancements...

* Updated the inputmap version `158` -> `185` (March 2026).
  * [Merged with latest default config](https://github.com/SpoddyCoder/x4-controller-config/commit/3e03cf9bc047056156bb7be228fa6206fdf14346) to capture game updates to control bindings since 2023.
  * See [changelog](./CHANGELOG.md).
* TODO: Preserve default keyboard + mouse functionality for seamless mixed use.
  * Acheived by updating the Steam Controller config to use different keys mapped to the modifiers.

## Usage
* Setup Steam controller support per [Eillis' guide](https://steamcommunity.com/sharedfiles/filedetails/?id=2954560643).
* Drag `inputmap_5.xml` into your `<Your documents>/Egosoft/X4/<numbers>/` folder.
  * If you're just the sort of person to have a 5th controller profile already, I probably don't need to tell you to take a backup before overwriting it.
* Load the 5th controller profile in-game.

### Modifying
* Docs and commit history should be helpful to anyone who wants to configure Eillis' setup to their own tastes. 
* Remember to save to profile 5 as you make changes, this will serve as your backup.
* If you want to track your changes in git, see [Setup For Dev](#setup-for-dev).

## Version History: `versions/`
* `158_1_eillis.xml` - Eillis' original config. `v158` spec, 1st profile slot.
* `185_1_default.xml` - latest default config shipped with the game. `v185` spec, 1st profile slot.
* `185_5_default-eillis.xml` - latest default config merged with Eillis' config. `v185` spec, 5th profile slot.
* `185_4_spoddycoder.xml` - my config, uses default-eillis as a base, modded for a "FPV" drone flight style. `v185` spec, 4th profile slot.
  * See [spoddycoder.md](./versions/docs/spoddycoder..md) for more details.

## Setup For Dev
Making changes to the **in-game** `inputmap_5.xml` should be reflected directly in the checked out repo version, so we can see the diff and commit changes.

* Run `cmd` (as admin) and create a link to the config file in the game directory to wherever you've checked out the repo, eg:
* `mklink "C:\Users\{USERNAME}\Documents\Egosoft\X4\10112698\inputmap_5.xml" "C:\Users\{USERNAME}\x4-controller-config\inputmap_5.xml"`
* You can ofc use any of the versions, eg:
* `mklink "C:\Users\{USERNAME}\Documents\Egosoft\X4\10112698\inputmap_4.xml" "C:\Users\{USERNAME}\x4-controller-config\versions\185_4_spoddycoder.xml"`

### WSL dev limitations
* Getting a link between a file located on the WSL instance and a file on the windows host is problematic - the two approaches you might try both have issues...
  * Cannot simply move the repo to a windows mounted dirctory on the WSL instance - this has performance + other issues when using an IDE on the host.
  * Not sure it's possible to have the windows host application (x4) access a file on a WSL instance filesystem.
    * Even if you could - this would mean you now require the WSL instance running to use the config... not ideal.
* Recommend you just use the windows host directly for this project.

## Eilli's Layout Reference
When no modifier buttons are held:
* A = A button as single press, W key as double press.
* B = B button as single press, S key as double press.
* X = X button as single press, Z key as double press.
* Y = Y button as single press, U key as double press.
* Back = Back as single press, C as double press.
* Start = Start as single press, N as double press.
* Left bumper = Left bumper.
* Right bumper = Right bumper.

Holding X button generally works like holding Ctrl on keyboard.
* A = Ctrl+A keys as single press, Ctrl+W keys as double press.
* B = Ctrl+B keys as single press, Ctrl+S keys as double press.
* X = (Held as modifier.)
* Y = Ctrl+Y keys as single press, Ctrl+U keys as double press.
* Back = Ctrl+V keys as single press, Ctrl+C keys as double press.
* Start = Ctrl+M keys as single press, Ctrl+N keys as double press.
* Left bumper = Ctrl+L key.
* Right bumper = Ctrl+R key.

Holding Y button generally works like holding Shift on keyboard.
* A = Shift+A keys as single press, Shift+W keys as double press.
* B = Shift+B keys as single press, Shift+S keys as double press.
* X = Shift+X keys as single press, Shift+Z keys as double press.
* Y = (Held as modifier.)
* Back = Shift+V keys as single press, Shift+C keys as double press.
* Start = Shift+M keys as single press, Shift+N keys as double press.
* Left bumper = Shift+L keys.
* Right bumper = Shift+R keys.

Holding Back turns some buttons into numbers, with double presses being numpads.
* A = 1 key as single press, Num 1 as double press.
* B = 2 key as single press, Num 2 as double press.
* X = 3 key as single press, Num 3 as double press.
* Y = 4 key as single press, Num 4 as double press.
* Left bumper = 5 key.
* Right bumper = 6 key.

Holding Start turns DPad into F keys.
* DPad Up = F1
* DPad Left = F2
* DPad Right = F3
* DPad Down = F4
* Left bumper = plus key.
* Right bumper = minus key.

### In-game
1.Triggers/Joysticks = flying axes.

2. Without modifiers:
* A = Acceleration, double press for Boost.
* B = Deceleration, double press for Full Stop.
* X = Deploy Countermeasure.
* Y = Target Hostile, double press for Target Object.
* LB = Primary weapon fire.
* RB = Secondary weapon fire.
* DPad Up = Switch ammunition.
* DPad Left = Scan.
* DPad Down = Magnet.
* Back = Interact, double press for Quick Action Menu.
* Start = Map, double press for Options Menu.

3. Holding X generally deals with weapons and combat systems.
* X + LB = Next primary weapon.
* X + RB = Next secondary weapon.
* X + DPad Up = Aim assist.
* X + DPad Left = Turrets.
* X + DPad Right = Drones.
* X + DPad Down = Flight assist.
* X + Start = Missions.

4. Holding Y generally deals with targetting.
* Y + B = Match target speed.
* Y + X = Target lock.
* Y + Start = Property owned.
* Y + DPad = Change target/subsystem.

5. Holding Back generally deals with ship systems and interactions.
* Back + A = Travel mode, double press for Autopilot.
* Back + B = Dock, double press for Get Up From Chair.
* Back + X = Comm, double press for Object Info.
* Back + Y = Scanner mode, double press for Long Range Scanner mode.
* Since Back + A/B/X/Y/LB/RB act as 1-6 keys, they are also used for NPC interactions. This is additionaly intuitive, considering Back is used for initiating an interaction.

6. Holding Start generally deals with camera.
* Start + DPad = Camera Up/Down/Left/Right.
* Start + LB = Cycle camera.
* Start + RB = Target camera.
* Start + LT = Zoom in.
* Start + RT = Zoom out.

7. When in map/menu mode, I usually use joystick to control cursor and joystick presses as mouse clicks.

## Contributing
PR's are welcome for any changes that would benefit everyone using this config. Just fork it if it's a personal preference thing, innit.

