# Repository context

This is a standalone CS2 config and crosshair-code collection. It lives inside a separate offline training-kit workspace, but this repository contains only the files in this directory.

- Preserve the owner's supplied commands and crosshair codes exactly unless they request changes. Do not silently repair or reformat codes.
- `follow-recoil.cfg` is executable CS2 console text. `crosshairs.txt` is a reference file: each entry uses a `#player` label followed by its code.
- Keep the README synchronized with filenames, installation steps, and observed limitations.
- Do not add credentials, external runtime dependencies, telemetry, match ingestion, or game automation.
- Do not publish surrounding training-kit files or personal data.
- No build or automated test suite is needed for this text-only collection. Use `git diff --check` and compare supplied content exactly before committing. The parent training-kit builder and verifier do not validate these files.
- In-game QA means loading the config, checking console errors, confirming both toggle states and colors, and separately testing crosshair imports. Do not claim this has passed without running it.
