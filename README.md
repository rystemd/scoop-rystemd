# Scoop bucket for rystemd

[Scoop](https://scoop.sh) bucket for the [rystemd](https://github.com/rystemd/rystemd)
project: the `rystemd` init/unit manager, the `rystemctl` systemctl-compatible
CLI, and the `rystemd-tui` terminal UI for Windows.

## Install

Add the bucket, then install:

```powershell
scoop bucket add rystemd https://github.com/rystemd/scoop-rystemd
scoop install rystemd/rystemd
```

This installs three commands onto your PATH:

- `rystemd` — the manager daemon (run it as a service first).
- `rystemctl` — the `systemctl`-compatible control CLI.
- `rystemd-tui` — the terminal UI.

The manifest pulls the portable Windows zip from the [latest GitHub
release](https://github.com/rystemd/rystemd/releases) and auto-updates to each
tagged version (`checkver`/`autoupdate`); the pinned hash is refreshed by
`scoop update` on new releases.

For a machine-wide Windows installer rather than a portable binary, use the
`rystemd-<ver>-x86_64.msi` asset on the same release page.

## Layout

- `bucket/rystemd.json` — the app manifest (points at release ZIP assets).
- `LICENSE` — MIT (the same license as the project).

The manifest is regenerated per release by the packaging in the
[rystemd](https://github.com/rystemd/rystemd) repository; keep the pinned hash
and `autoupdate` URL in sync with the released asset names.