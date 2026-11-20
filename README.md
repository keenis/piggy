# piggy

## Install

```powershell
scoop bucket add piggy https://github.com/keenis/piggy
```

## Manifests

| App | What it is |
| --- | --- |
| `breeze` | Flutter comic reader, comic sources via plugins |
| `cloudy` | Third-party NetEase Cloud Music client (liquid-glass UI) |
| `diskgenius-cn` | DiskGenius 中文版 — partition manager / data recovery (free tier) |
| `dns-benchmark` | dnspy — bulk DNS resolver benchmark with a visual dashboard |
| `mpv_PlayKit` | mpv-lazy config bundle (shaders, filters, Chinese-annotated conf) |
| `mygo-music` | Native plugin-extensible music player |
| `ths-ai` | 同花顺AI版 — the stock client formerly known as 同花顺远航版 |
| `yuumi` | Yuumi — League of Legends in-game companion (Tauri, portable zip) |

## Notes

- Manifests are updated automatically by
  [Excavator](https://github.com/ScoopInstaller/GithubActions) (`checkver` + `autoupdate`),
  except the ones listed below.
- `ths-ai` has no `checkver` on purpose: the vendor's version API is a release-notes feed
  that lags behind the download CDN, so autoupdate would downgrade the pinned build.
  Bump it by hand — see the `##` key in the manifest.
- `ths-ai` was renamed from `ths-yhb` when upstream dropped the 远航版 branding for AI版.
  Renaming a manifest changes the app name, so an existing `ths-yhb` install has to be
  reinstalled to pick up this one.
- `mpv_PlayKit` keeps the upstream project's camelCase name rather than this bucket's
  lowercase-hyphen style, so that it stays greppable against the upstream repo.
