# Canada Network X-Ray

An interactive, mobile-friendly map that exposes the physical and organizational layers underneath Canada's Internet.

## What is mapped

- The 22 Hurricane Electric Canadian PoPs supplied for this project, checked against HE's public Canada PoP directory.
- Twelve Canadian Internet exchange metros listed by CIRA.
- Switchable, **schematic** corridor layers for Bell, Rogers, TELUS, Zayo/Allstream and regional carriers.
- Interconnection-gravity and geographic-chokepoint lenses.
- **Route Passport**, a local in-browser traceroute visualizer accepting CSV columns: `hop,lat,lon,carrier,asn,rtt_ms`.

## Accuracy model

Three categories are deliberately kept separate:

1. **Public site**: a street address published by the operator; map coordinates are approximate to that address.
2. **Exchange metro**: city-level placement, not necessarily the exchange switch's exact room.
3. **Schematic corridor**: a readable city-to-city abstraction from public network materials, never a representation of surveyed fibre ducts or a guaranteed BGP path.

Do not use the map for excavation, emergency operations, physical access, or claims about live routing. Infrastructure and BGP policy change continuously.

## Open it

Open `index.html` in a modern browser. It is a static Leaflet app and needs network access for the basemap and Leaflet CDN.

For a zero-install preview:

`https://htmlpreview.github.io/?https://github.com/hiighbob/canada-network-xray/blob/main/index.html`

## Best next data layers

- PeeringDB facility, network and IXP API records.
- ISED National Broadband Data (GeoPackage, 250 m road segments).
- ISED Spectrum Management System licensed radio sites.
- CIRA Canadian Traceroute Database exports.
- TeleGeography submarine cable landing data.
- Provincial open-data fibre projects and grants.
- Live RIPE Atlas measurements, with uncertainty shown for every geolocated hop.

## Sources

- Hurricane Electric Canada PoPs: https://pop.he.net/?country=Canada
- CIRA IXPs: https://www.cira.ca/en/net-good/network-resilience/ixps/
- CIRA Canadian Traceroute Database: https://www.cira.ca/en/net-good/ctrd-psc/
- ISED National Broadband Data: https://open.canada.ca/data/en/dataset/00a331db-121b-445d-b119-35dbbe3eedd9
- PeeringDB: https://www.peeringdb.com/
- ISED Spectrum Management data: https://ised-isde.canada.ca/site/spectrum-management-telecommunications/en/spectrum-allocation/spectrum-management-system-data
- TeleGeography 2026 submarine cable map: https://submarine-cable-map-2026.telegeography.com/

## License

MIT for project code. Third-party datasets and basemap tiles remain under their respective licences and terms.
