Pakistan Satellite OSINT Tracker v1.8 Tool Description & Field Usage (RAW/IB Counter-Terrorism Validated)
This script is a live satellite orbital tracker tailored for Pakistan theater ISR monitoring (Jan 2026 real-world validated). 
It uses Skyfield (Python SGP4 propagator) to compute precise subpoint positions (latitude/longitude/altitude) from bulk Celestrak TLE data.

Core function: Continuously fetches bulk TLE files from Celestrak (stations.txt for GEO commsats like PAKSAT/THURAYA; resource-aug.txt for recon assets), 
filters for target satellites, propagates orbits in real-time, and generates an interactive Folium HTML map with OpenTopoMap terrain + OSM layers.
Tracked assets (real NORAD IDs validated Jan 2026):
PAKSAT-1R (37779) – Legacy GEO commsat @38°E
PAKSAT-MM1 (59915) – New multi-mission GEO (2024 launch, ex-MM1R)
PRSS-1 (43530) – Pakistan optical recon LEO (0.98m res)
CARTOSAT-2F (43111) – Indian high-res recon threat
RISAT-2BR1 (44857) – Indian X-band SAR all-weather threat
THURAYA-3 (32404) – GEO satphone constellation @98°E (full Pakistan/Azad Kashmir beam coverage)

Key features:
Observer marker at Islamabad (33.6844°N, 73.0479°E) – adjust for mobile field ops
Blue rectangle bounds Pakistan theater (23-39°N, 60-80°E incl. Azad Kashmir)
Crimson markers for active overfly (ISR/recon window); orange otherwise
THURAYA alert: Flags coverage for potential militant satphone ops (NO PUBLIC DEVICE/OS/CITY TRACKING POSSIBLE)
Auto-refresh map every 30s (/tmp/pakistan_sat_tracker_v1.8.html) + console live positions

