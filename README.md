# Plex Meta Manager - Configs för TV och Filmer
## Detta innehåller endast metadata med länkar till TheposterDB och themoviedb.org

Denna GitHub är **Work In Progress** All metadata och affischer är från TheposterDB.org. Användaren Musikmann2000 står för nästan alla affischer som vi använder oss av men en del är egengjorda.

Dessa config-filer är anpassade till [Plex Meta Manager :nightly](https://metamanager.wiki/en/latest/index.html)-branch.

Glöm inte och följa [Trash-guides](https://trash-guides.info/) för att namnge ditt bibliotek på ett korrekt sätt!


Finns inte din TV Serie eller Film så finns det en template https://github.com/Ninja-FSE/pmm-config/tree/main/tv/metadata som du kan använda dig utav och lägga till en Request, använd sedan ```Issues```
Glöm inte att använda kod-taggning annars blir formateringen fel.

# HOWTO

I Plex Meta Manager config lägg till

```yaml
custom_repo: https://github.com/Ninja-FSE/pmm-config/tree/main/
```

Sedan under TV biblioteket, metadata_path lägg till

```yaml
- repo: metadata/tv/tvshows
- repo: overlays/subtitles # Detta lägger till en Svensk flagga i högra nedre hörn om TV-Serien har svenskt text.
```

Sedan under Film biblioteket, metadata_path lägg till
```yaml
- repo: metadata/movies/movies
- repo: overlays/subtitles # Detta lägger till en Svensk flagga i högra nedre hörn om Filmen har svenskt text.
 ```