# Mappinest

Mappinest is developer-first map infrastructure for hosting and delivering geospatial data through standard APIs. It was developed as an alternative to map cloud providers such as Mapbox, MapTiler, and Esri. The goal is to provide predictable hosting costs and detailed usage analytics, and to give you more control over your data and infrastructure. Mappinest provides infrastructure optimized for vector and raster tile delivery, with built-in caching and support for the map clients you already use.

You can upload `MBTiles`, `PMTiles`, or `GeoJSON`, create and edit datasets, secure access with API keys and domain restrictions, and use the same URLs with MapLibre GL JS, Mapbox GL JS, OpenLayers, Leaflet, desktop GIS tools, and server-side workflows. Available map styles use open standards and can also be self-hosted on your own infrastructure.

## What Mappinest Provides

- **Tiles API** hosts your `MBTiles` and `PMTiles` tilesets and delivers vector or raster tiles through a CDN.
- **Maps API** provides available map styles that map clients load through [StyleJSON](https://www.mappinest.com/docs/maps-api/stylejson).
- **Dataset API** lets you upload `GeoJSON` or create editable datasets, edit features, and serve them as `GeoJSON`.
- **API keys** with scopes and domain restrictions control who can use your maps and data.
- **Usage analytics** show requests by API key, tileset, dataset, domain, country, and device.
- **Free plan** includes monthly usage. No card required.

## Useful Links

- [Website](https://www.mappinest.com)
- [Documentation](https://www.mappinest.com/docs)
- [Get an API key](https://www.mappinest.com/console/keys)
- [Pricing](https://www.mappinest.com/pricing)
- [Tiles API](https://www.mappinest.com/docs/tiles-api)
- [Maps API](https://www.mappinest.com/docs/maps-api)
- [Dataset API](https://www.mappinest.com/docs/dataset-api)
- [Examples](https://github.com/mappinest/examples)
- [Status](https://status.mappinest.com)
- [Changelog](https://www.mappinest.com/docs/reference/changelog)


## Recommended Integration Paths

- [StyleJSON](https://www.mappinest.com/docs/maps-api/stylejson) for loading available map styles through the Maps API.
- [TileJSON](https://www.mappinest.com/docs/tiles-api/tilejson) for loading uploaded tilesets through the Tiles API.
- [GeoJSON](https://www.mappinest.com/docs/dataset-api/geojson) for loading a dataset through the Dataset API.

## Code Snippets

**Maps API with MapLibre GL JS**

Load a MapLibre GL JS map with an available map style using StyleJSON.

```js
const apiKey = 'YOUR_MAPPINEST_KEY';

const map = new maplibregl.Map({
  container: 'map',
  style: `https://api.mappinest.com/v1/maps/streets/style.json?key=${apiKey}`,
  center: [12, 48],
  zoom: 4
});
```

**Tiles API with MapLibre GL JS**

Add a vector tileset source to an existing MapLibre GL JS map using TileJSON. 
 Replace `YOUR_TILESET_ID` with your [tileset ID](https://www.mappinest.com/docs/console/upload-data#tileset-naming) from the console.

```js
const apiKey = 'YOUR_MAPPINEST_KEY';
const tilesetId = 'YOUR_TILESET_ID'; // username.tileset-name

map.on('load', () => {
  map.addSource('my-tileset', {
    type: 'vector',
    url: `https://api.mappinest.com/v1/tiles/${tilesetId}.json?key=${apiKey}`
  });
});
```

## Example Integrations

The examples below use MapLibre GL JS. The repo has the same examples for [Mapbox GL JS](https://github.com/mappinest/examples/tree/main/examples/mapbox-gl-js), [OpenLayers](https://github.com/mappinest/examples/tree/main/examples/openlayers), and [Leaflet](https://github.com/mappinest/examples/tree/main/examples/leaflet). Replace `YOUR_MAPPINEST_KEY` with your API key.

- [Add an uploaded vector tileset](https://github.com/mappinest/examples/tree/main/examples/maplibre-gl-js/uploaded-vector-tileset)
- [Add an uploaded raster tileset](https://github.com/mappinest/examples/tree/main/examples/maplibre-gl-js/uploaded-raster-tileset)
- [Load a map style](https://github.com/mappinest/examples/tree/main/examples/maplibre-gl-js/stylejson-map-style)
- [Add an editable GeoJSON dataset](https://github.com/mappinest/examples/tree/main/examples/maplibre-gl-js/dataset-geojson)
