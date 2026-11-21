# DSH boot animation package

This repo is the Grok-娘 / 鲸鱼娘 boot-animation and chat-wallpaper package for DeepSeek Harness on Windows PC `DESKTOP-I3L4FME`.

**Zip:** `dsh-boot-setup.zip`  
**Size:** 7888150 bytes  
**SHA256:** `b645091962c29d8989555cdc41deca15e4ef8331d34057999aeac048bb369bc8`

The same files are also included already extracted, so you can copy them without unzipping.

## Windows paths (do not change the username)

Copy configs and assets into `C:\Users\诚诚\.dsh\` so they land exactly here:

- `C:\Users\诚诚\.dsh\dsh-startup.json`
- `C:\Users\诚诚\.dsh\chat-wallpaper.json`
- `C:\Users\诚诚\.dsh\chat-wallpaper\dsh-wallpaper-v3a.png`
- `C:\Users\诚诚\.dsh\startup-templates\custom-halfface-v3\template.json`
- `C:\Users\诚诚\.dsh\startup-templates\custom-halfface-v3\assets\import-halfface-v3.mp4`

Creating missing folders is fine.

**Do not** delete or rewrite unrelated files, especially `cordis.patch.yml`. Leave `cordis.patch.yml.bak-timeout` alone. `whale-purse` is disabled in the patch; do not re-enable it. Do not change the plugin-manager `githubConnectionTimeoutMs: 30000` row.

You can either copy the extracted files from this repo, or expand `dsh-boot-setup.zip` into `C:\Users\诚诚\.dsh\`. After unzipping, confirm the five paths above exist.

## Install the boot plugin

Only one boot plugin should be active. Install the official package **LeeRolling/dsh-boot-suite** (MIT), not some other plugin.

Desktop CLI (not on PATH):

```powershell
$dsh = 'C:\Users\诚诚\AppData\Local\Programs\DeepSeek Harness\resources\runtime\cli\bin\dsh.cmd'
& $dsh plugin --profile desktop add dsh-boot-suite
```

Profile: `C:\Users\诚诚\.dsh\profiles\desktop`  
DSH version last seen: `0.2.2-rc.3`

If the CLI command needs a GitHub/npm URL, use `LeeRolling/dsh-boot-suite`. You can also install it from the DSH plugin market if that is easier. If GitHub access fails because there is no VPN, retry after a VPN is on, or install from the market.

## After install: full restart (required)

Do **not** auto-kill DSH if it may be mid-work. The user must fully quit DeepSeek Harness, including the tray icon, then reopen it once.

## Package contents (for checking)

- `dsh-startup.json` — act 1 default (`"template": "archive-warm"`), act 2 is `"act2": "custom-halfface-v3"`, dissolve 600ms, act2 video sound off
- `chat-wallpaper.json` — image path `C:\Users\诚诚\.dsh\chat-wallpaper\dsh-wallpaper-v3a.png`, imageFit cover, bgMode image, colorMode color, default veils
- `chat-wallpaper/dsh-wallpaper-v3a.png`
- `startup-templates/custom-halfface-v3/template.json` — id `custom-halfface-v3`, name “Grok娘与鲸鱼娘半脸线稿”, duration 17667, video layer src `import-halfface-v3.mp4` at 1280×720
- `startup-templates/custom-halfface-v3/assets/import-halfface-v3.mp4`
