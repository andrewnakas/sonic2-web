# sonic2-web

Sonic the Hedgehog 2 in the browser, bring your own ROM. Live at
https://andrewnakas.github.io/sonic2-web/ and listed on https://decompgames.com.

**No game data is in this repository or on the page.** You pick your own ROM; it is read
in the tab and never uploaded.

## What this is

- **Source project:** [sonicretro/s2disasm](https://github.com/sonicretro/s2disasm) at `8571731799cb5ecc5ff81b5a7740fcfa9fc3c0f0 (classics branch)`.
- **Matching build:** The classics branch reassembles the Rev B program and data exactly; with the retail header checksum restored (two bytes) the ROM has SHA-1 `2af1003247aec262089c8df22d05e80d04a1b5e4`, identical to the Sonic Classics cartridge image. The master branch builds REV01 (`8bca5dcef1af3e00098666fd892dc1c2a76333f9`).
- **Browser player:** [mdcore](https://github.com/andrewnakas/mdcore), this fleet's MIT-licensed Mega Drive core (freestanding WebAssembly). This is emulation of the rebuilt ROM, not a native
  port of the game's code to WebAssembly.

## Tested

Rev B booted through the title into Emerald Hill Zone and ran right under keyboard input on mdcore (muted, headless). Audio has not been listened to: every test ran muted. Nothing
beyond that scope has been played.

## Layout

- `web/` — the page (published as the `gh-pages` branch).
- `web/THIRD-PARTY-NOTICES.txt` — licences of the vendored runtime.
