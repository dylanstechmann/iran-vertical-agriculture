# Iran Vertical Agriculture Concept — 3D Visualization & Outline

## Overview
This package is a **concept model** for high-tech, controlled-environment agriculture in Iran, built as a clean, labeled, multi-scene Blender file. It is organized at three scales:

1. **National network** — a stylized Iran map with six representative production hubs.
2. **Regional campus** — a 10-hectare-style site with grow halls, greenhouse, water treatment, solar, and packhouse.
3. **Pilot facility** — a detailed indoor-building cutaway with racks, utility rooms, and routed systems.

The model is **illustrative**, not construction-ready. It uses **metric units** (1 Blender unit = 1 metre) and is intended for planning discussions, presentations, and as a visual reference for a more detailed engineering effort.

## What’s included
- `iran_vertical_agriculture.blend` — six named scenes, each with its own camera and sun light.
- `renders/` — six 1920×1080 PNG renders.
- `countries.geojson` — public-domain Natural Earth admin-0 country outline used as the source boundary.
- `iran_boundary_simplified.json` — simplified boundary and center coordinates used by the national map scene.
- `README.md` — this outline and legend.
- The rural-Florida scenario track now lives in its own repository; see "Side scenario: rural Florida" below.

## Scene index
| Scene | Purpose | Camera |
|---|---|---|
| `IranVA_Index` | Title card, shared color legend, and scene list | `IndexCam` |
| `IranVA_National` | Stylized Iran map with six production hubs and example links | `NationalCam` |
| `IranVA_Campus` | Regional campus layout with buildings, roads, solar, and utilities | `CampusCam` |
| `IranVA_Pilot` | Pilot-building cutaway with racks, rooms, and routed systems | `PilotCam` |
| `IranVA_Rack` | Four-tier NFT hydroponic rack detail with plumbing and airflow | `RackCam` |
| `IranVA_Utilities` | Node-link schematic of water, nutrient, power, HVAC, controls, and waste | `UtilitiesCam` |

## National network (`IranVA_National`)
- Extruded, stylized Iran silhouette built from a simplified public-domain Natural Earth outline.
- Six representative production hubs, each with a short adaptation note:
  - **Tehran / Alborz** — research, training, urban production.
  - **Central arid (Isfahan / Yazd)** — cooling, water recovery, solar.
  - **Northwest (Tabriz)** — winter heating, insulation.
  - **Northeast (Mashhad)** — seasonal heating / cooling, regional supply.
  - **South (Shiraz / Bandar Abbas)** — heat rejection, water-quality management.
  - **North (Rasht)** — dehumidification, disease control.
- Example distribution links radiate from Tehran to the other hubs.
- The map is a **concept illustration**, not survey or political-boundary data.

## Regional campus (`IranVA_Campus`)
- Two indoor grow halls.
- High-tech greenhouse with a simple pitched roof.
- Water treatment plant with clean-water and raw-water tanks.
- Purge / waste tank.
- Nutrient / fertilizer storage with separate A and B tanks.
- Packhouse and cold storage.
- Training and admin building.
- Solar array field.
- Water reservoir.
- Expansion pad for a second phase.
- Roads and color-coded utility corridors:
  - **Blue** — water supply and return lines.
  - **Green** — nutrient lines.
  - **Orange** — electrical / solar power.
  - **Purple** — control and sensor wiring.
  - **Red** — purge / waste lines.

## Pilot facility cutaway (`IranVA_Pilot`)
- 20 × 12 m schematic building footprint.
- Roof and front wall removed to show the interior.
- Functional zones:
  - Entry / airlock / office.
  - Nursery / propagation.
  - Leafy-green hydroponic racks.
  - Fruiting-crop drip-substrate zone.
  - Nutrient / fertilizer room.
  - Water treatment / recirculation room.
  - Electrical / controls / PLC room.
  - Packing / cold storage.
- Three four-tier grow racks with shelves, LED strips, and simple plant placeholders.
- HVAC ducts and fans.
- Routed water, return, nutrient, power, control, purge, and condensate lines.
- A legend identifies each subsystem color.

## Grow-rack detail (`IranVA_Rack`)
- Four-tier NFT hydroponic rack.
- Channels, plants, and LED grow bars on each shelf.
- Water and nutrient manifolds, valves, and sensor boxes.
- Airflow duct, fan unit, and vent.
- Drip-fed substrate pots for fruiting crops.
- Labels call out channels, LED bars, manifolds, sensors, airflow, and drip irrigation.

<!-- SPLIT -->
## Utility-system schematic (`IranVA_Utilities`)
A node-link diagram showing how the main systems connect:
- Source water intake.
- Filtration.
- Disinfection / UV.
- Clean-water tank.
- Nutrient dosing with A + B concentrates.
- Grow zones.
- Return lines / sump.
- Purge / waste handling.
- Condensate recovery.
- Solar panels / power.
- Grid / backup power.
- HVAC / dehumidifier.
- PLC / sensors.
- Packhouse / cold storage.
- Wastewater reuse.

Color-coded flows show water, nutrient, power, controls, and waste routing.

## Crops and growing systems
| Production system | Suitable crops |
|---|---|
| Multi-tier NFT or DWC hydroponics | Lettuce, leafy greens, basil, mint, dill, coriander, microgreens |
| Ebb-and-flow nursery benches | Vegetable seedlings and transplant production |
| Indoor stacked or rotated modules | Strawberries, subject to pollination and economic testing |
| High-tech greenhouse with drip-fed substrate | Tomatoes, cucumbers, peppers |
| Efficient field or orchard systems | Wheat, rice, pistachios, saffron, and other crops that are usually **not** economical as vertical-farm products |

This distinction is deliberate: tall fruiting crops need substantial vertical space and light, and staple grains or orchard crops should not be presented as economical vertical-farm products.

## Water management
- **Loop:** source water → filtration → disinfection → clean-water tank → nutrient dosing → crop zones → filtered return → disinfection / monitoring → recirculation.
- Separate potable-water and agricultural process-water plumbing.
- Flow, pressure, tank-level, EC, pH, temperature, and leak sensors.
- Zone isolation valves, sampling ports, drains, bypasses, and backflow prevention.
- Filtration plus UV or another engineered disinfection stage.
- Condensate recovery where measured water quality and regulations permit.
- Controlled, nutrient-rich purge handling rather than claiming “zero discharge.”
- RO or desalination only where source-water analysis justifies it, including responsible concentrate disposal.
- Dashboard metrics: **liters per kilogram of saleable produce** and **percentage of water recirculated**.

## Fertilizer / nutrient management
- Separate **A and B concentrate tanks** to keep incompatible concentrates from mixing prematurely.
- Isolated, safely handled acid or pH-control storage.
- Automated dosing driven by EC and pH, with alarms and manual fallback.
- Crop-specific recipes rather than one fertilizer blend for everything.
- Regular laboratory verification because sensors alone do not measure every nutrient.
- Root-zone oxygen, temperature, and drainage monitoring.
- Inventory tracking, spill containment, calibration, and sanitation procedures.

## Electricity, HVAC, and controls
- Grid connection with submetering for LEDs, HVAC, pumps, refrigeration, and controls.
- Rooftop or nearby solar PV, with batteries sized by reliability and economic requirements.
- Backup power prioritized for controls, water circulation, refrigeration, and other critical loads.
- High-efficiency LEDs controlled by **PPFD / DLI targets**, not fixed full-power operation.
- Zoned HVAC, dehumidification, airflow, filtration, and heat recovery.
- Temperature and humidity coordinated through **vapor-pressure-deficit** targets.
- Load scheduling that does not compromise crop health or food safety.
- Honest energy accounting: solar panels are **not** automatically assumed to power the entire indoor farm.

## Automation and operations
- Local PLC control that continues safely if internet service is interrupted.
- Sensor dashboards, alarms, maintenance logs, and crop traceability.
- Manual overrides and safe failure states.
- Integrated pest management and biosecurity.
- Cybersecurity, user permissions, and backed-up control configurations.
- Pilot evaluation metrics: water/kg, energy/kg, saleable yield, labor, crop losses, and operating margin.

## Visual legend
| Color | Meaning |
|---|---|
| Light gray | Country outline / structural / floor |
| Blue | Water system |
| Dark blue | Return / drain lines |
| Green | Nutrient system and crop production |
| Orange | Electricity / solar |
| Purple | Controls / sensors |
| Red | Waste / purge |
| Light blue | Production hub marker |

## Side scenario: rural Florida (separate repository)

A second, separately labeled scenario track adapts the same controlled-environment pattern to rural Florida: elevated flood-aware grow halls, a CUPS-style insect-exclusion screenhouse for citrus (oranges), high-value crops such as pea shoots, herbs, strawberries, tomatoes and peppers, solar plus battery storage, rainwater harvest, and hurricane/flood resilience.

It began inside this repository under `side-quests/rural-florida/` and has moved to its own standalone repository so it can be published and updated independently: https://github.com/dylanstechmann/rural-florida-agriculture (now public as well). There it keeps the same pattern: config-driven assumptions (`config/scenario.json`), a generated planning report (`docs/scenario-report.md`) pinned by tests, local-first automation, N+1 redundancy, a qualification ladder (simulated day → wet test → commissioning → first crop-cycle audit), and its own 3D visualizations (scenes `FLRural_Index`, `FLRural_Campus`, `FLRural_Systems`).

All Florida-side numbers remain labeled placeholder arithmetic, never measurements or designs.

## Engineering and data caveats
- The model is a **concept illustration**, not a construction document.
- The national map is a **simplified stylized outline**, not survey data.
- Hub locations are approximate city coordinates used for placement only.
- Water, energy, yield, and cost figures are **design targets**, not performance claims.
- Real deployment requires site-specific civil, mechanical, electrical, plumbing, and agricultural engineering, plus permits, water rights, grid studies, market research, and local agronomy.

## How to open
1. Open `iran_vertical_agriculture.blend` in **Blender 4.x or later**.
2. Use the scene dropdown in the top bar to switch between the six named scenes.
3. Each scene already has one active camera and one sun light.
4. Press `F12` or use the **Rendering** workspace to render the current scene.
5. The model uses **metric units**: 1 Blender unit = 1 metre.

## Notes on CAD
Blender was sufficient for these visualizations. For fabrication-ready parts or precise assembly drawings, export the relevant geometry from Blender or rebuild it in a CAD package such as FreeCAD or OpenSCAD. OpenSCAD was **not** necessary for this stage of the project.

---
*Built as a concept visualization for high-tech controlled-environment agriculture in Iran. Not engineering, survey, or construction data.*