<div align="center">
  <img src=".assets/hianime-logo.png" alt="hianime.at" width="200">
  <p><strong>Watch anime from your terminal.</strong></p>

  <p>
    <a href="https://github.com/armoox/ani-cli-enhanced/wiki/Installation">Install</a> •
    <a href="https://github.com/armoox/ani-cli-enhanced/wiki/Usage">Usage</a> •
    <a href="https://github.com/armoox/ani-cli-enhanced/wiki/FAQ">FAQ</a> •
    <a href="https://github.com/armoox/ani-cli-enhanced/wiki">Wiki</a>
  </p>

  <p>
    <img src="https://img.shields.io/badge/license-GPLv3-blue" alt="License">
    <img src="https://img.shields.io/badge/shell-POSIX-green" alt="POSIX">
  </p>
</div>

---

A fork of [pystardust/ani-cli](https://github.com/pystardust/ani-cli) — built around [hianime.at](https://hianime.at) with CDN-tolerant playback

### Features

- **Buffer that stays seekable** — mpv gets a symmetric RAM window (`--cache-size`, default 1GiB) *plus* a disk-spilled cache (`--cache-on-disk`, default on), so you can scrub forward **and** backward through the whole episode or movie without re-buffering; dropped shard-CDN connections auto-reconnect (lavf) and a network timeout caps how long a dead connection can stall rather than freezing playback
- **Rich search** — results show type & duration, the id slug is hidden, and menus can page through every result (`-P/--page` or the "load more" entry)
- **Download manager** — per-anime folders (`$DOWNLOAD_DIR/One Piece/Episode 1.mp4`), `--batch` for whole series, and concurrent downloads (`--parallel N` / `ANI_CLI_PARALLEL`)
- **Skip intro & outro** — bundled MyAnimeList-based integration that needs no `ani-skip` binary (`--skip` / `ANI_CLI_SKIP_INTRO`)
- **Auto-play & resume** — rolls into the next episode automatically (`--auto-play`) and picks up exactly where you left off (`-c --resume`)
- **Full playback control** — quality picker (`-q`), dubs, episode/count ranges (`-e 5-6`), in-terminal playback (`--no-detach`), VLC or Syncplay

### Quick start

```sh
curl -sL https://raw.githubusercontent.com/armoox/ani-cli-enhanced/master/install.sh | sudo sh
```

### Learn more

| Topic | Link |
|-------|------|
| 📦 Installation | [Installation guide](https://github.com/armoox/ani-cli-enhanced/wiki/Installation) |
| 🎮 Usage & flags | [Usage guide](https://github.com/armoox/ani-cli-enhanced/wiki/Usage) |
| ❓ Questions | [FAQ](https://github.com/armoox/ani-cli-enhanced/wiki/FAQ) |
| 🗑️ Uninstall | [Uninstallation](https://github.com/armoox/ani-cli-enhanced/wiki/Uninstallation) |
| 🔄 Update | [Update & Patch](https://github.com/armoox/ani-cli-enhanced/wiki/Update-and-Patch) |
