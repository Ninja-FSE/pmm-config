# Plex Meta Manager - Configs för TV och Filmer
## Detta innehåller endast metadata med länkar till TheposterDB och themoviedb.org

Denna GitHub är **Work In Progress** All metadata och affischer är från TheposterDB.org. Användaren Musikmann2000 står för nästan alla affischer som vi använder oss av men en del är egengjorda.

Dessa config-filer är anpassade till [Plex Meta Manager :nightly](https://metamanager.wiki/en/latest/index.html)-branch.

Glöm inte och följa [Trash-guides](https://trash-guides.info/) för att namnge ditt bibliotek på ett korrekt sätt!


Finns inte din TV Serie eller Film så finns det en template https://github.com/Ninja-FSE/pmm-config/tree/main/tv/metadata som du kan använda dig utav och lägga till en Request, använd sedan ```Issues```
Glöm inte att använda kod-taggning annars blir formateringen fel.

# HOWTO
## Användning via GitHub
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

## Användning lokalt. OBS DENNA METOD GÖR SÅ ATT DU MISSAR UPPDATERINGAR
För att installera detta på din server så clona/ladda ner repo'n. lägg filerna som dom ligger rakt in i din Plex Meta Manager mapp och justera din Plex Meta Manager config fil så att den ser ut som följande

```yaml
libraries:
  Movies:
    operations:
      sync_tags: true
      add_blank_entries: false
    metadata_path:
    - folder: metadata/movies/movies
    overlay_path:
    - folder: overlays/subtitles

  TV:
    metadata_path:
    - folder: metadata/tv/tvshows
    overlay_path:
    - folder: overlays/subtitles
    - remove_overlays: false
    - reapply_overlay: true
 ```