# Metadata For TV Shows

# Request new shows using ```Issues```
## Use this Template

```yaml
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


Dont forget to use code brackets or the formating will be wrong!!