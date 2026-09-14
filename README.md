<div align="center">
  <img src="https://hianime.at/theme/images/logo.png" alt="hianime.at" width="200">
  <p><strong>Watch anime from your terminal.</strong></p>

  <p>
    <a href="https://github.com/armoox/ani-cli-fork/wiki/Installation">Install</a> •
    <a href="https://github.com/armoox/ani-cli-fork/wiki/Usage">Usage</a> •
    <a href="https://github.com/armoox/ani-cli-fork/wiki/FAQ">FAQ</a> •
    <a href="https://github.com/armoox/ani-cli-fork/wiki">Wiki</a>
  </p>

  <p>
    <img src="https://img.shields.io/badge/license-GPLv3-blue" alt="License">
    <img src="https://img.shields.io/badge/shell-POSIX-green" alt="POSIX">
  </p>
</div>

---

A fork of [pystardust/ani-cli](https://github.com/pystardust/ani-cli) — built around [hianime.at](https://hianime.at) with CDN-tolerant playback

### Features

- **Rich search** — results show type & duration, with page-through menus (`-P/--page` or the "load more" entry)
- **Download manager** — per-anime folders (`$DOWNLOAD_DIR/One Piece/Episode 1.mp4`) and parallel `--batch` downloads (`--parallel N` / `ANI_CLI_PARALLEL`)
- **Skip intro & outro** — bundled mpv integration queries [aniskip.com](https://aniskip.com) via the MyAnimeList id (no `ani-skip` binary needed; `--skip` / `ANI_CLI_SKIP_INTRO`)
- **Auto-play** — keeps playing the next episode when one ends (`--auto-play`); combine with `-c --resume` to pick up a series where you left off

### Quick start

```sh
curl -sL https://raw.githubusercontent.com/armoox/ani-cli-fork/master/install.sh | sudo sh
```

### Learn more

| Topic | Link |
|-------|------|
| 📦 Installation | [Installation guide](https://github.com/armoox/ani-cli-fork/wiki/Installation) |
| 🎮 Usage & flags | [Usage guide](https://github.com/armoox/ani-cli-fork/wiki/Usage) |
| ❓ Questions | [FAQ](https://github.com/armoox/ani-cli-fork/wiki/FAQ) |
| 🗑️ Uninstall | [Uninstallation](https://github.com/armoox/ani-cli-fork/wiki/Uninstallation) |
| 🔄 Update | [Update & Patch](https://github.com/armoox/ani-cli-fork/wiki/Update-and-Patch) |
