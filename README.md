# Plex Meta Manager - Configs for TV and Movies
## This only contains metadata with links to TheposterDB and themoviedb.org

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
- repo: overlays/subtitles # This is adding the Swedish flags if PMM finds Swedish subtitles
```

then under your Movie Library, metadata_path add
```yaml
- repo: metadata/movies/movies
- repo: overlays/subtitles # This is adding the Swedish flags if PMM finds Swedish subtitles
 ```


# Request new Shows/Movies using ```Issues```
## Use this Template

```yaml
###################################################################
#                                                                 #
#  Your Request Show/Movie (YEAR)                                 #
#                                                                 #
###################################################################
    "Your Request show (YEAR)": # TV Show Name
        year: YEAR  # Year, example 2023
        title: "Your Request Show" # This is how Plex is showing it as, this is quite sensetive
        url_poster: https://theposterdb.com/api/assets/349096 # Please only use posters from the creator MusikMann2000 or similuar posters
        match:
          mapping_id: 75219 # Show ID from https://www.themoviedb.org
        seasons:
            1:
                url_poster: https://theposterdb.com/api/assets/349097 # Use Season posters from the same creator
            2:
                url_poster: https://theposterdb.com/api/assets/349098
```


Dont forget to use code brackets or the formating will be wrong!!