# drone-map

A map of where drones may and may not be flown, starting with the **Netherlands** and **South Africa**.

Status: early planning. No data has been pulled or verified yet. Every source below must be checked against the authority's own publication before the app relies on it.

## Scope (v1)

- Netherlands (NL)
- South Africa (ZA)

## Planned data model

Each zone record stores:

- `country`: NL or ZA
- `zone_type`: controlled airspace, restricted, prohibited, airport, nature/protected area, urban/crowd, other
- `altitude_limit`: lower and upper bound, if given
- `rule_authority`: the body that owns the rule (for example ILT, LVNL, SACAA, ATNS)
- `source_url` and `source_license`
- `last_checked`: date the source was last verified

This lets the app say "restricted by X, see Y" without hardcoding each country's rules.

## Sources to verify

### Netherlands

- Drone rules: ILT (Inspectie Leefomgeving en Transport), applied alongside EU Regulation 2019/947.
- Airspace and AIP: LVNL (Luchtverkeersleiding Nederland).
- Aggregators: OpenAIP, OpenStreetMap (ODbL, attribution required).
- Open question: whether ILT or LVNL publishes a drone geo-zone feed, and its license.

### South Africa

- Drone rules: SACAA (South African Civil Aviation Authority), CAR Part 101.
- Airspace and AIP: ATNS (Air Traffic and Navigation Services).
- Aggregators: OpenAIP, OpenStreetMap (ODbL, attribution required).
- Open question: whether ATNS or SACAA publishes a drone map or API, and whether restricted areas are available as data.

## Disclaimer

Flight rules change and depend on local conditions. This project is not a substitute for the official rules or a pre-flight check with the relevant authority.
