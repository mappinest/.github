# Mappinest

Mappinest is developer-first map infrastructure for hosting and delivering map tiles and map styles through standard APIs. It was developed as an alternative to map cloud providers such as Mapbox, MapTiler, and Esri. The goal is to provide **predictable hosting costs**, detailed usage analytics, and more control over your data and infrastructure.

Mappinest provides production-ready **vector and raster tile delivery** with **built-in caching** while you keep using the map clients you already know. You can upload `MBTiles` or `PMTiles`, secure access with API keys and domain restrictions, and use the same URLs with MapLibre GL JS, Mapbox GL JS, OpenLayers, Leaflet, desktop GIS tools, and server-side workflows.

Map styles are available through the Maps API, use standard StyleJSON, and can also be self-hosted on your own infrastructure.

## Start Here

- [Website](https://www.mappinest.com)
- [Documentation](https://www.mappinest.com/docs)
- [Tiles API](https://www.mappinest.com/docs/tiles-api)
- [Maps API](https://www.mappinest.com/docs/maps-api)
- [Pricing](https://www.mappinest.com/pricing)
- [Public examples](https://github.com/mappinest/examples)
- [Status & uptime](https://status.mappinest.com)
- [Changelog](https://www.mappinest.com/docs/reference/changelog)


## What Mappinest Provides

- Tile hosting for uploaded vector and raster tilesets
- Available map styles for web map integrations
- TileJSON metadata for uploaded tilesets
- API key authentication and domain restrictions
- Cache-friendly URL patterns for production maps
- Usage analytics for production map delivery
- Examples for MapLibre GL JS, Mapbox GL JS, OpenLayers, and Leaflet

## Example Integrations

Use the public examples repo when you want copy-ready projects instead of isolated snippets.

- [Load a Mappinest map style](https://github.com/mappinest/examples/tree/main/examples/maplibre-gl-js/stylejson-map-style)
- [Add an uploaded vector tileset](https://github.com/mappinest/examples/tree/main/examples/maplibre-gl-js/uploaded-vector-tileset)
- [Add an uploaded raster tileset](https://github.com/mappinest/examples/tree/main/examples/maplibre-gl-js/uploaded-raster-tileset)
- [Leaflet.VectorGrid vector tileset example](https://github.com/mappinest/examples/tree/main/examples/leaflet/leaflet-vectorgrid)

## Core Concepts

- `StyleJSON` describes available Mappinest map styles.
- `TileJSON` describes uploaded tilesets and their tile endpoints.
- `MBTiles` and `PMTiles` are accepted tileset upload formats.
- `YOUR_MAPPINEST_KEY` is the placeholder used in copy-ready examples.

For implementation details, start with the [docs](https://www.mappinest.com/docs) or open the [examples repo](https://github.com/mappinest/examples).
