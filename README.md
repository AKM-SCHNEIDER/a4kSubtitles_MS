<img align="left" width="115px" height="115px" src="icon.png">

# AKM Subtitles

[![Kodi version](https://img.shields.io/badge/Kodi-20--21-blue)](https://kodi.tv/)

AKM Subtitles is a multi-source subtitle addon for Kodi. It is an independent,
side-by-side install of the a4kSubtitles codebase: installing it does not
replace the original a4kSubtitles addon.

## Subtitle providers

- Addic7ed
- BSPlayer
- OpenSubtitles
- Podnadpisi.NET
- SubDL
- SubSource

## Improvements in AKM Subtitles

- Uses Kodi's playing-media metadata when it is available.
- Falls back to parsing a release filename, such as `Some.Show.S02E04.1080p.mkv`,
  to recover the title, year, season, and episode.
- Supports manual text searches from Kodi's subtitle search action.
- Can keep searching when Kodi does not provide an IMDb ID; supported providers
  receive the available title and episode metadata.
- Optionally resolves incomplete titles through TMDb. Add a personal TMDb API
  key in **Add-on settings → Accounts** to enable this fallback.
- Retains multi-provider searches and file-hash matching where a provider
  supports them.

## Installation

A public Kodi repository URL has not been published yet. Until one is available,
install a ZIP package created from this project through Kodi's **Install from zip
file** option.

Once the repository is published, its copy-and-paste URL and installation steps
will be listed here.

## Configuration

Configure provider accounts/API keys under **Add-on settings → Accounts**.
TMDb is optional, but improves matching for poorly labelled streams and manual
searches.

## Development

Configure hooks to refresh the generated `packages/addons.xml` manifest:

```sh
git config core.hooksPath .githooks
```

## Attribution and license

AKM Subtitles is a modified distribution of
[a4kSubtitles](https://github.com/a4k-openproject/a4kSubtitles) by its original
authors. It is distributed under the [MIT License](LICENSE); the original
copyright notice and license are retained.

## Icon

Logo `quill` by Ramy Wafaa ([RoundIcons](https://roundicons.com)).
