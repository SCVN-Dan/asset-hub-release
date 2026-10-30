# Asset Hub

Browse Unity projects on GitHub, preview models, prefabs and VFX, and export them with all their dependencies as a `.unitypackage`.

This repo holds only the **built app** (no source code). Download it from **[Releases](https://github.com/SCVN-Dan/asset-hub-release/releases/latest)**.

## Requirements

- A Mac with **Apple silicon (M1, M2, M3, M4)**. To check: click  (top left) › **About This Mac** › **Chip**. Intel Macs are not supported.
- An internet connection during install (the app is about 90 MB).
- A GitHub account that is a member of the company organization, with read access to the asset repos.

## Install

1. Open the **[latest release](https://github.com/SCVN-Dan/asset-hub-release/releases/latest)** and download **`Asset-Hub-Installer.dmg`** (about 1 MB).
2. Open the downloaded `.dmg`, then open **Cài Asset Hub** (the installer) in the window that appears.
3. **First time only:** macOS blocks the installer because it is not notarized by Apple. Allow it once:
   - **macOS 15 (Sequoia) or later**
     1. Click **Done** on the warning.
     2. Open **System Settings** › **Privacy & Security** and scroll to the bottom.
     3. Next to *"Cài Asset Hub" was blocked…*, click **Open Anyway**, enter your Mac password, then click **Open**.
   - **macOS 14 (Sonoma) or earlier:** **right-click** **Cài Asset Hub** › **Open**, then click **Open**.
4. Click **Cài đặt** (Install). The installer:
   - downloads the latest Asset Hub from this repo (with a progress bar),
   - checks the file against its SHA-256 checksum,
   - installs it into **Applications** (or `~/Applications` if your account cannot write to Applications),
   - opens Asset Hub.

   Asset Hub itself opens without any security warning.
5. You can now eject and delete the installer `.dmg`.

## Sign in

1. In Asset Hub, click **START**.
2. If the GitHub CLI is not on your Mac, the app downloads it automatically (no admin rights needed).
3. A **room code** appears and is copied for you. Click **Open GitHub**, paste the code, click **Continue**, then **Authorize**.
4. Go back to Asset Hub — the chest opens and you are in.

Next time you open the app, it goes straight to the hub.

Alternatively, click **Use a token instead** at the bottom of the start screen and paste a fine-grained personal access token with read access to the asset repos.

## Update

Run **Cài Asset Hub** again. It always downloads the latest release and replaces the installed version; your settings and cache are kept.

## Uninstall

1. Quit Asset Hub and drag it from **Applications** to the **Trash**.
2. Optional: to remove downloaded data and thumbnails too, delete `~/Library/Application Support/asset-hub` (in Finder: **Go › Go to Folder…** and paste the path).

## Troubleshooting

| Problem | What to do |
|---|---|
| *"Asset Hub chỉ chạy trên Mac chip Apple…"* | This Mac has an Intel chip, which is not supported. |
| *"Không tải được Asset Hub từ GitHub (mã lỗi …)"* (download failed) | Check your internet connection and that `github.com` is reachable (VPN/proxy), then run the installer again. The error code and message help when reporting the problem. |
| *"File tải về không khớp mã kiểm tra…"* (checksum mismatch) | The download was corrupted or a release was being published. Wait a minute and run the installer again. |
| The installer cannot be opened at all | Follow step 3 of [Install](#install) to allow it once. |
| Sign-in works but no repos appear | Your GitHub account needs to be invited to the company organization and have access to the asset repos. Ask your lead. |
