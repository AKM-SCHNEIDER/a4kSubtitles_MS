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

### Install the Kodi repository

#### Method 1: Install from the GitHub Pages ZIP directly

1. Download the repository installer ZIP:
   https://akm-schneider.github.io/a4kSubtitles_MS/packages/
2. In Kodi, open **Settings → Add-ons → Install from zip file**.
3. Select the downloaded repository ZIP and install it.
4. Then go to **Add-ons → Install from repository → AKM Subtitles Repository**.
5. Install **AKM Subtitles**.

#### Method 2: Add the GitHub Pages folder as a Kodi source

1. In Kodi, open **Settings → File manager**.
2. Select **Add source**.
3. Select **<None>** and paste:
   https://akm-schneider.github.io/a4kSubtitles_MS/packages/
4. Give the source a name, for example: **AKM Repo**.
5. Go to **Add-ons → Install from zip file**.
6. Open the source you just added and select:
   `repository.akmsubtitles-1.0.0.zip`
7. Install the repository.
8. Then go to **Add-ons → Install from repository → AKM Subtitles Repository**.
9. Install **AKM Subtitles**.

### Install the add-on ZIP directly

If you already have the package locally, you can also install the add-on ZIP from
Kodi using **Install from zip file**:

- `service.subtitles.akmsubtitles-3.24.3.zip`

The repository installer is the recommended method, because it keeps the add-on
updated through the GitHub Pages repository.

## Configuration

Configure provider accounts/API keys under **Add-on settings → Accounts** for SubDl, Subsource. and you will need the username and password for the Opensubtitles.
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
