# Homebrew ZSearch Tap

Official Homebrew Cask tap for [ZSearch](https://zsearch.ai) — data-sovereign AI search and document platform for macOS.

## Install

```sh
brew tap zsearch-ai/zsearch
brew install --cask zsearch
```

Or as a one-liner:

```sh
brew install --cask zsearch-ai/zsearch/zsearch
```

## Update

```sh
brew upgrade --cask zsearch
```

ZSearch also has an in-app auto-updater (electron-updater) — both paths stay in sync via the same release feed.

## Uninstall

```sh
brew uninstall --cask zsearch          # keep user data
brew uninstall --zap --cask zsearch    # also wipe documents, settings, logs
```

## Requirements

- macOS 13 Ventura or later
- Apple Silicon (arm64) only — Intel Mac support pending

## Verifying the signature

The release is signed by **PYKS Pty Ltd** (Apple Developer Team ID `3X6VAH672Y`) and notarized by Apple. To verify locally:

```sh
codesign -dv --verbose=4 /Applications/ZSearch.app
spctl -a -vv /Applications/ZSearch.app
xcrun stapler validate /Applications/ZSearch.app
```

All three should report success without warnings.

## License

This tap repository is MIT licensed. The ZSearch application itself is under its own license — see https://zsearch.ai for terms.
