# Mappinest

Mappinest is developer-first map infrastructure for hosting and delivering map tiles and map styles through standard APIs.

Upload `MBTiles` or `PMTiles`, secure access with API keys and domain restrictions, and use the same URLs in MapLibre GL JS, Mapbox GL JS, OpenLayers, Leaflet, desktop GIS tools, and server-side workflows.

## Start Here

- [Mappinest website](https://www.mappinest.com)
- [Documentation](https://www.mappinest.com/docs)
- [Map client guides](https://www.mappinest.com/docs/guides)
- [Tiles API](https://www.mappinest.com/docs/tiles-api)
- [Map Styles API](https://www.mappinest.com/docs/styles-api)
- [Pricing](https://www.mappinest.com/pricing)
- [Public examples](https://github.com/mappinest/examples)

## What Mappinest Provides

- Tile hosting for uploaded vector and raster tilesets
- StyleJSON delivery for available map styles
- TileJSON metadata for map-client integrations
- API key authentication and domain restrictions
- Cache-friendly URL patterns for production maps
- Examples for MapLibre GL JS, Mapbox GL JS, OpenLayers, and Leaflet

## Example Integrations

Use the public examples repo when you want copy-ready projects instead of isolated snippets.

- [Load a Mappinest map style](https://github.com/mappinest/examples/tree/main/examples/maplibre-gl-js/stylejson-map-style)
- [Add an uploaded vector tileset](https://github.com/mappinest/examples/tree/main/examples/maplibre-gl-js/uploaded-vector-tileset)
- [Add an uploaded raster tileset](https://github.com/mappinest/examples/tree/main/examples/maplibre-gl-js/uploaded-raster-tiles)
- [Leaflet.VectorGrid vector tileset example](https://github.com/mappinest/examples/tree/main/examples/leaflet/leaflet-vectorgrid)

## Core Concepts

- `StyleJSON` describes available Mappinest map styles.
- `TileJSON` describes uploaded tilesets and their tile endpoints.
- `MBTiles` and `PMTiles` are accepted tileset upload formats.
- `YOUR_MAPPINEST_KEY` is the placeholder used in copy-ready examples.

For implementation details, start with the [docs](https://www.mappinest.com/docs) or open the [examples repo](https://github.com/mappinest/examples).
