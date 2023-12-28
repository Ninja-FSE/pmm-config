# Plex Meta Manager - Configs för TV och Filmer
## Detta innehåller endast metadata med länkar till TheposterDB och themoviedb.org

Denna GitHub är **Work In Progress** All metadata och affischer är från TheposterDB.org. Användaren Musikmann2000 står för nästan alla affischer som vi använder oss av men en del är egengjorda.

Dessa config-filer är anpassade till [Plex Meta Manager :nightly](https://metamanager.wiki/en/latest/index.html)-branch.

Glöm inte och följa [Trash-guides](https://trash-guides.info/) för att namnge ditt bibliotek på ett korrekt sätt!


Finns inte din TV Serie eller Film så finns det en template https://github.com/Ninja-FSE/pmm-config/tree/main/tv/metadata som du kan använda dig utav och lägga till en Request, använd sedan ```Issues```
Glöm inte att använda kod-taggning annars blir formateringen fel.

# HOWTO

Nedan är ett exempel hur din Plex Meta Manager config fil borde se ut som för att få våra configs att funka!

```yaml
libraries:
  Movies:
    operations:
      sync_tags: true
      add_blank_entries: false
    metadata_path:
    - repo: metadata/movies/movies
    overlay_path:
    - repo: overlays/subtitles

  TV:
    metadata_path:
    - repo: metadata/tv/tvshows
    overlay_path:
    - repo: overlays/subtitles
    - remove_overlays: false
    - reapply_overlay: true

settings:
  custom_repo: https://github.com/Ninja-FSE/pmm-config/tree/main/
 ```