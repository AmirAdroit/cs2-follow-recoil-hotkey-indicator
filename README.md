# CS2 follow recoil hotkey indicator

A small collection of CS2 settings: an N-key follow-recoil toggle with a color indicator, plus saved crosshair codes.

## Files

- `follow-recoil.cfg`: the supplied console commands, preserved exactly.
- `crosshairs.txt`: saved crosshair codes with player labels. The `#donk` label and code were supplied by the repository owner; attribution and import validity have not been independently verified.
- `AGENTS.md`: maintenance instructions.

## Load the config

1. In Steam, open Counter-Strike 2's installed files using **Browse**.
2. Copy `follow-recoil.cfg` into `game/csgo/cfg/` under that installation. Make sure the filename ends in `.cfg`, not `.cfg.txt`.
3. Enable the developer console in CS2's game settings.
4. Open the console and run:

```text
exec follow-recoil
```

The intended initial state is follow recoil off with a green crosshair. Press **N** to toggle follow recoil and switch the red/green RGB values. The visible color depends on your existing crosshair settings. Executing the file replaces any previous N-key binding.

To load it on each launch, add this line to your existing `autoexec.cfg`:

```text
exec follow-recoil
```

Back up your existing config and N-key binding before applying this file. To undo it, remove the added autoexec line and restore your previous crosshair settings and N binding.

## Saved crosshairs

Open `crosshairs.txt` and copy the code beneath the desired `#player` label. Paste it into CS2's crosshair **Share or Import** dialog. Codes are stored verbatim; if CS2 rejects a code, obtain a fresh export rather than guessing changes to it.

## Verification and limitations

The files are plain text. No build, dependencies, environment variables, server, credentials, or game automation are required.

The supplied snippet is preserved verbatim, including `cl_crosshaircolor_a`. It has not been tested in a running CS2 client. Check the console for unknown commands and test both N-key states in practice before relying on the indicator. Changing follow recoil or RGB values separately can desynchronize the state and color; rerun `exec follow-recoil` to reset the supplied values.

Maintain this repository with `git diff --check` and an in-game smoke check after command changes. Keep a copy of your personal settings for rollback; Git stores this repository's files, not your live game configuration.
