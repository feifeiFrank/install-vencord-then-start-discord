# Discord with Vencord Portable v0.2.2

This release fixes a macOS launcher regression caused by building the Vencord Installer from the upstream `main` branch.

## What's new

- macOS launcher now checks out the official Vencord Installer release tag `v1.4.0` before building the CLI
- Avoids breakage when upstream development code on `main` is temporarily not buildable
- Keeps the official Vencord data path: `~/Library/Application Support/Vencord/dist`
- Keeps the official Installer CLI `repair` flow before launching Discord
- Advanced users can override the installer tag with `VENCORD_INSTALLER_TAG`

## Notes

- First macOS launch still needs internet access so the Installer CLI can fetch the latest Vencord release files.
- macOS users still need permission to modify `/Applications/Discord.app`.
- If macOS blocks the normal patch attempt, approve the administrator prompt or grant the launcher App Management / Full Disk Access.
- Installer logs are written to `/tmp/vencord-portable-install.log`.
