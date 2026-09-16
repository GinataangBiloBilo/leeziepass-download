# LeeziePass

A memorable password generator for IT admins — a small Windows GUI tool, no
install, no dependencies, single portable `.exe`.

Diceware-style: it picks 1–3 random words from a wordlist, optionally applies
phonetic spelling-confusion swaps (so the words *sound* the same but are
harder to guess by typing the "obvious" spelling), then adds a 2–4 digit
number and a special character at randomised positions. Every password gets
at least one uppercase and one lowercase letter, a digit, and a symbol.

## Download

Grab the latest release from the [Releases page](../../releases/latest):

- `leeziepass.exe` — the app. Just run it, nothing to install.
- `sample-wordlist.txt` — a small demo wordlist to try the custom-wordlist
  feature (see below).
- `SHA256SUMS.txt` — checksums for the above, if you want to verify your
  download before running it.

To verify on Windows (PowerShell):

```powershell
Get-FileHash leeziepass.exe -Algorithm SHA256
```

Compare the printed hash against the one in `SHA256SUMS.txt`.

## Using it

1. Pick which built-in wordlists feed the generator: **Dutch**, **German**,
   **English** — check any combination, they get combined into one pool.
2. Toggle **Phonetic transforms** if you want the spelling-confusion swaps.
3. Click **Generate Passwords** for 5 candidates, and **Copy** the one you want.
4. **Export to .txt** writes a batch of freshly generated passwords (you
   choose how many) to a text file, one per line — handy for provisioning
   several accounts at once.

### Using your own wordlist

Click **Browse...** and pick any plain text file — one word per line, `#` for
comments, at least 20 words. Try it with `sample-wordlist.txt` above. Once a
custom list is loaded, the three checkboxes switch from "which built-in
lists to combine" into "which language's phonetic rules apply to this list"
— pick whichever fits your wordlist's spelling best.

A SHA-256 hash of whatever file you load is shown next to it, so you can
confirm you loaded the file you think you loaded.

### About / licenses

Right-click the title bar (or the app icon, top-left) for **About LeeziePass**
and **Third-Party Licenses** — the latter opens the full attribution notices
for the open-source components this app is built on (all MIT/Apache-2.0,
no copyleft).

## Source

This repository ships the compiled binary and usage docs only; the source
is maintained privately.
