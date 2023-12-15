# Metadata

If you dont want to use the ```- repo: ``` in your pmm config you can git clone this repo and use ```- folder:``` instead to bulk load all the single files that you can find in folder ```shows```

Both ```tvshows.yml``` and ```shows``` are updated at the same time!

# Request new shows using ```Issues``` or create a ```Pull Request```
## Use this Template

```
###################################################################
#                                                                 #
#  TV-Shows Your Request show (YEAR)                              #
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