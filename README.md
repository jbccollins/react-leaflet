# React-Leaflet-Extendable 

[![npm version](https://img.shields.io/npm/v/react-leaflet-extendable.svg)](https://www.npmjs.com/package/react-leaflet-extendable)

This is literally just a fork of [react-leaflet](https://github.com/PaulLeCam/react-leaflet) that adds the ability to directly extend components. Unless you have an issue specifically about extending components DO NOT raise issues here. Raise them on the [react-leaflet](https://github.com/PaulLeCam/react-leaflet/issues) repository.

At the moment I an not personally using this library. If this gets too out of date and there's a feature missing here that react-leaflet has then just raise an issue or make a PR and I'll rebase as soon as I can.

This repository exists because of https://github.com/PaulLeCam/react-leaflet/issues/506

Please read through that issue before deciding if you actually should use this library and not react-leaflet. For most use cases react-leaflet will be fine.

TLDR;
react-leaflet v2 makes it impossible to directly extend these components:

- AttributionControl
- Circle
- ExtendableCircle
- FeatureGroup
- GeoJSON
- ImageOverlay
- LayerGroup
- LayersControl
- Marker
- Pane
- Polygon
- Polyline
- Popup
- Rectangle
- ScaleControl
- TileLayer
- Tooltip
- VideoOverlay
- WMSTileLayer
- ZoomControl

This fork lets you extend those.

The extendable exports of these components are all formatted like: `Extendable<COMPONENT>`

e.g. `ExtendableAttributionControl`, `ExtendableCircle`, etc...

## Usage
```javascript
import { ExtendableTileLayer, withLeaflet } from 'react-leaflet-extendable'

class MyCustomTileLayer extends ExtendableTileLayer {
    // Go nuts here
}
export default withLeaflet(MyCustomTileLayer)
```

## License

MIT\
See [LICENSE](LICENSE) file.
