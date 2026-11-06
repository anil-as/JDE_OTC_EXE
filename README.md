# OTC48 Windows downloads

This repository contains the OTC48 installer and update files. Users do not need
a GitHub account to download the installer or receive updates.

## Install or upgrade

Download **OTC48.exe** from the latest published release and run it. Choose your
installation folder. Existing users should choose their current OTC48 folder;
no uninstall is needed. After setup finishes, close setup and open the OTC48 desktop
shortcut. Workbooks, reports, settings, and saved JDE login are preserved.

If no release has been published yet, open `OTC48.exe` in this repository and
use GitHub's **Download raw file** button to download the installer.

## Files to upload for a release

Current version: **1.0.11**

| File | Purpose | Needed by |
| --- | --- | --- |
| `OTC48.exe` | Small Windows installer; contains application files and templates | Users and the updater |
| `OTC48-update.json` | Version, download size, and SHA-256 used to verify updates | Automatic updater |

Users normally download only **OTC48.exe**. The publisher uploads **both
files from the same tested build** as release assets. Keep their filenames intact.
The manifest already includes the installer SHA-256. The separate checksum and
user guide are optional support files that can remain local.

## Publish the first release

1. Open [Create a release](https://github.com/anil-as/JDE_OTC_EXE/releases/new).
2. Create tag **v1.0.11** targeting **main**. Use title **OTC48 1.0.11**.
3. Attach the two files listed above using the release asset upload area.
4. Publish as a stable release and select **Set as the latest release** if shown.
   Do not select prerelease or leave the release as a draft.

**Files committed to the repository are not release assets.** Attach the two
files to the GitHub Release too; the automatic updater reads release downloads.
Automatic checks work after a stable release has been published.

## Later updates

Build and test a higher application version, then create a stable release tagged
`v<version>` with its matching two assets. Never mix an installer and update
manifest from different builds.

OTC48 checks for updates on startup once every 24 hours. Users can check
immediately with menu **9. Check for updates**. They accept the update, exit
after setup, and reopen the desktop shortcut. No GitHub sign-in is required.

Keep this repository limited to distribution files. Do not add local `.env`
files, saved credentials, user workbooks, run reports, dependency folders, or
development history. The EXE itself contains extractable application code and
templates; it is not a source-code secrecy mechanism.

## GitHub's Source code archive links

GitHub automatically generates Source code (zip) and Source code (tar.gz) links
from the distribution repository at the release tag. These are not separately
uploaded assets and do not contain the private development repository. Existing
tags may include the earlier optional guide/checksum files as well.

The public EXE itself contains extractable automation code and templates. Use
access-controlled company hosting if those contents must remain confidential.
