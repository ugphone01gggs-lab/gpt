# Predictive Buffer v3.0

**Unified** predictive input buffer for Geometry Dash 2.2 (Geode), based on the best of:

- **Click Before Frames** (basu.input-buffer) by BASU
- **Afterflow** by prsevend

### What it does

Geometry Dash runs physics at 240 ticks/s. When you press or release early, a hidden "ghost" player is simulated with delayed versions of that input. If a delayed version survives clearly longer, your real input is held back and delivered on the safer tick.

Works for cube, ship, ball, UFO, wave, robot, spider, swing + orbs, pads, gravity/speed/size/mode portals.

**This is a cheat.** Do not use on rated levels or for legit claims.

### Platforms

- Windows
- Android (32 + 64-bit)
- macOS

### Key features in v3.0

- Full Android support with touch-friendly UI
- **Auto-hide panel** while playing (so it never blocks the screen on phones)
- Panel opacity + scale settings
- Completely reorganized settings (categories: General, Panel, Stages, Orbs, Modes, Advanced, Auto, Debug, Keybinds)
- All advanced prediction options retained (orb timing, level memory, mode-smart, etc.)
- Geode keybinds (rebindable, works without F-keys)
- In-game console + Buffer menu accessible from Pause
- Performance mode + auto budget for weaker devices

### Default controls

| Action              | Default key |
|---------------------|-------------|
| Cycle stage         | F6          |
| Open Buffer menu    | F8          |
| Show/hide console   | F9          |
| Path view           | F10         |
| Copy log            | F11         |
| Forget level memory | F7          |

On Android you can change these in Geode settings / keybinds, and use the **Buffer** button in the Pause menu + **Console** button inside the menu.

### Important settings for mobile

- **Auto-hide panel while playing** → ON (default)
- **Panel opacity** / **Panel scale** → adjust for your screen
- **Prediction time budget** → try 4–8 ms on phones
- **Performance mode** → enable if you get hitches
- **Practice mode only** → recommended

### Building

Requires Geode SDK and a working GD 2.2081 toolchain for the target platform.

```bash
# set GEODE_SDK, then
cmake -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build
```

The resulting `.geode` goes into the game's `geode/mods` folder.

### Credits

- Original Click Before Frames / predictive buffer work by BASU and contributors
- Afterflow by prsevend (terminal approach, some fixes, stage ideas)
- Geode team
- Community testers

### Warning

Using this on rated levels, leaderboards, or anything you want to claim as legit is cheating. Some levels/lists detect input buffers / macros.
