# Plex Meta Manager - Configs för TV och Filmer.
## Detta innehåller endast metadata med länkar till TheposterDB, themoviedb.org och thetvdb.com.

Denna GitHub är **Work In Progress** All metadata och affischer är från TheposterDB.org. Användaren Musikmann2000 står för nästan alla affischer som vi använder oss av men en del är egengjorda.

Dessa config-filer är anpassade till [Plex Meta Manager :nightly](https://metamanager.wiki/en/latest/index.html)-branch.

Glöm inte och följa [Trash-guides](https://trash-guides.info/) för att namnge ditt bibliotek på ett korrekt sätt!


Öppna en ````Issue```` om din film eller serie inte finns så lägger vi till den

# HOWTO
## Användning via GitHub.
Nedan är ett exempel hur din Plex Meta Manager config fil borde se ut som så att Plex Meta Manager läser filerna från GitHub utan att behöva ha filerna på din server.

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

## Användning lokalt.
### OBS DENNA METOD GÖR SÅ ATT DU MISSAR UPPDATERINGAR.
För att installera detta på din server så clona/ladda ner repo'n. lägg filerna som dom ligger rakt in i din Plex Meta Manager mapp och justera din Plex Meta Manager config fil så att den ser ut som följande.

```yaml
libraries:
  Movies:
    operations:
      sync_tags: true
      add_blank_entries: false
    metadata_path:
    - file: metadata/movies/movies.yml
    - folder: metadata/movies/collections
    overlay_path:
    - folder: overlays/subtitles

  TV:
    metadata_path:
    - file: metadata/tv/tvshows.yml
    - folder: metadata/tv/collections
    overlay_path:
    - folder: overlays/subtitles
    - remove_overlays: false
    - reapply_overlay: true
 ```