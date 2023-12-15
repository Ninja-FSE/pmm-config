# Plex Meta Manager - Configs for TV and Movies

This is **Work In Progress** posters are from TheposterDB.org and almost all posters are from the great Musikmann2000.

To request please use Issues or Pull Requests.
A Request Template can be found https://github.com/Ninja-FSE/pmm-config/tree/main/tv/metadata


# HOWTO

In Plex Meta Manager config add

```yaml
custom_repo: https://github.com/Ninja-FSE/pmm-config/tree/main/
```

then under your TV Library, metadata_path add

```yaml
- repo: metadata/tv/tvshows
- repo: overlays/subtitles
 # This is adding the Swedish flags if PMM finds Swedish subtitles
```

then under your Movie Library, metadata_path add
```yaml
- repo: metadata/movies/movies
- repo: overlays/subtitles
 # This is adding the Swedish flags if PMM finds Swedish subtitles
 ```