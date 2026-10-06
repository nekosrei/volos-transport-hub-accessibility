# Walking accessibility of a proposed transport hub in Volos, Greece

## Question
How accessible on foot is a proposed intermodal transport hub (urban/intercity bus stations, Sekeri St.) from the railway station, the passenger pier and key points of interest, and how much of the street network falls within the 500 m walking threshold used by SDG indicator 11.2.1?

## Method
- Walking network from OpenStreetMap (osmnx), ~3 km around Sekeri St.
- Points of interest located from OpenStreetMap data.
- Shortest walking routes on the street network (networkx), 75 m/min (4.5 km/h).
- Street length within 500 m and 1,000 m walking distance of the hub.
- Final map produced with matplotlib (Python).

## Results
| Destination | Straight line (m) | Walking (m) | Time (min) | Within 500 m |
|---|---|---|---|---|
| Intercity bus station | 79 | 61* | 0.8 | Yes |
| Info centre | 35 | 43* | 0.6 | Yes |
| Railway station | 479 | 820 | 10.9 | No |
| Town hall | 737 | 845 | 11.3 | No |
| Passenger pier | 1,041 | 1,554 | 20.7 | No |

- 13.4 km of streets lie within 500 m of the hub; 48.9 km within 1,000 m.
- Straight-line distance underestimates real walking distance, especially to the pier (1,041 m vs 1,554 m).
- The two bus stations are within the 500 m threshold; the railway station and the pier are not, which supports a shuttle/e-bike link.
- Cross-check: Google Maps gives 1.4 km / 20 min walking to the pier area.

## Limitations
- *Points are snapped to the nearest network node (19-38 m), which explains the small inconsistency in very short distances.
- Quality of the OpenStreetMap network and exact stop locations.
- Constant walking speed; no slopes, crossings or waiting times.
- Street length measures network coverage, not population.

## Context
Developed as a follow-up to my diploma thesis on sustainable transport hubs in the context of smart cities (University of Thessaly, 2026).

## Tools
Python, osmnx, networkx, geopandas, pandas, matplotlib, Google Colab.
