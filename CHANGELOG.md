# Changelog

All notable changes to ani-cli-enhanced are documented here.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

> The version number also drives the built-in `-U` updater: users on an older
> release are offered the update as soon as the new version lands on `master`.

## [5.4.0] - 2026-09-25

### Changed
- Streaming resilience: mpv now auto-reconnects dropped shard connections
  (`stream-lavf-o=reconnect=1,reconnect_streamed=1`) and a `--network-timeout=20`
  caps how long a dead connection can stall playback before it reconnects
  (mpv's default freeze is a full 60s)
- Embed page is now fetched with the hianime referer (some hosts 403 without one)
- Master playlist fetch retries once on a transient empty parse
- Scraping timeout is configurable via `ANI_CLI_HTTP_TIMEOUT` (default 20s,
  was a fixed 10s which could fail on slow embed/playlist pages)

### Fixed
- `-q 720p` (trailing `p`) now matches correctly instead of silently falling
  back to best quality; `-q 720` still works
- `--parallel 0` is rejected with a clear error instead of behaving erratically
- Parallel batch downloads no longer clobber each other's `/tmp` scratch files
  (`$$` is shared by sibling jobs; temp names are now per-episode)
- `--batch` no longer skips episodes whose previous download left a 0-byte file

## [5.3.0] - 2026-09-25

### Added
- `--cache-size` / `ANI_CLI_CACHE`: symmetric mpv buffer window so forward *and* backward seeking stays usable
- `--disk-cache` / `ANI_CLI_DISK_CACHE` (default on): spill the mpv stream cache to a temp file so long episodes remain seekable regardless of ram window
- `CHANGELOG.md`; scraper smoke-test CI workflow runs the live scraping chain nightly
- Diagnostic warnings in `hianime_m3u8` for each failure stage (missing server, undecodable embed, rotated obfuscation key, missing m3u8) instead of a bare "No sources found"

### Fixed
- `urlencode` now escapes `%` (first), so search queries containing a literal `%` no longer corrupt the `printf` search template
- Search menu hides the url slug and maps the picked display line back to its result row
- ShellCheck is fully clean (two info-level SC2094 notes silenced with a documented rationale)

### Changed
- Provider branding and install/docs references moved to the `ani-cli-enhanced` repo
- CI pins ShellCheck v0.10.0 and uses `actions/checkout@v7`

## [5.2.0] - 2026-09-14

### Added
- Premium search results (type & duration shown, paginated "load more" through `-P`/`--page`)
- `--parallel N` / `ANI_CLI_PARALLEL` concurrent episode downloads with `--batch`
- Intro/outro skipping with a bundled MyAnimeList-based integration (`--skip` / `ANI_CLI_SKIP_INTRO`), falling back to the `ani-skip` binary
- `--auto-play` / `ANI_CLI_AUTO_PLAY`: roll into the next episode automatically

## [5.1.3] - 2026-09-14

### Changed
- Provider switched from anineko.to to hianime.at, with logo updates

## [5.1.0-anineko] - 2026-09-10

### Changed
- Provider switched from the dead anidb.app to anineko.to, with CDN-tolerant playback and cache tuning for smooth segment delivery

## [5.0.x] - 2026-08

### Fixed
- Ported upstream v5 fixes (titles, `nth`, update flow, ani-skip), resume position tracking, `-e` validation and decimal episodes, cloudflare handling, flatpak_mpv dep check

## [4.x] - prior

History retained in git prior to the 5.0 line; see `git log` for details.