# Rural Florida side quest — high-tech agriculture concept

Private side quest to the Iran vertical-agriculture baseline in this repository.
Labeled scenario track: rural Florida, USA — flood-aware, storm-rated,
solar-plus-storage controlled-environment agriculture for higher-value crops.

Status: agent-drafted 2026-10-27 from the owner's direction. Labeled
placeholder assumptions only. No site is chosen, nothing here is
owner-reviewed or independently reviewed, and no number is a measurement,
price quote or performance claim. Regenerate outputs after editing the
scenario file; never hand-edit generated files.

## Why a side quest

The Iran baseline asks how controlled-environment agriculture adapts across a
large, water-constrained country. This track asks the same question for a
completely different environment: rural Florida — humid, hurricane-exposed,
flood-prone, rain-rich, with strong winter fresh-market demand and a
different pest and disease picture. Keeping it a labeled side quest (rather
than editing the baseline) is the pattern borrowed from the
AI/robot-parenting project: a scenario track beside a baseline, never
replacing it.

## What is shared with the Iran baseline

- The same color legend: blue water, green nutrients/crops, orange power,
  purple controls, red waste/purge, gray structure.
- The same scene pattern: index, campus, systems schematic.
- The same honesty rules: concept visualization and placeholder arithmetic,
  never engineering, survey or construction data.

## What is deliberately different

- Cooling and dehumidification instead of winter heating.
- Elevated, storm-rated, above-ground construction (raised-floor placeholder
  1.2 m). NOT an underground bunker: rural Florida means a high water table,
  flood exposure and hurricanes, so below-grade space is a liability there.
- Hurricane-rated ballasted PV racking, storm shutters/straps, a retention
  pond, and rainwater harvest sized against the water balance.
- Citrus (oranges) in a CUPS-style insect-exclusion screenhouse, not in
  stacked indoor racks: citrus is a tall, long-lived tree crop, and the
  Florida-relevant framing is psyllid/HLB exclusion research, not racks.
- High-value fresh crops first (pea shoots, herbs, strawberries, tomatoes,
  peppers). Peas are evaluated honestly: as pea shoots (fast turns, premium
  pricing, genuinely suited to racks) rather than as a bulk protein play.

## Structure

```
side-quests/rural-florida/
├── README.md                  # this file
├── pyproject.toml
├── config/scenario.json       # labeled placeholder assumptions
├── docs/
│   ├── crop-system-matrix.md          # hand-written crop reasoning
│   ├── water-energy-model.md          # model equations and regen instructions
│   ├── resilience-and-automation.md   # flood/storm resilience, N+1, local-first
│   └── scenario-report.md             # GENERATED report (tests pin it)
├── src/floridafarm/           # config loader, model, report renderer, CLI
├── tests/                     # unittest suite (stdlib only)
└── viz/
    ├── rural-florida-campus.blend   # FLRural_* scenes (separate from Iran blend)
    └── renders/                    # 1920x1080 PNG renders
```

## Run it

Python 3.10 or later, standard library only.

```bash
cd side-quests/rural-florida
PYTHONPATH=src python -m floridafarm validate                      # check the scenario file
PYTHONPATH=src python -m floridafarm report --out docs/scenario-report.md   # regenerate the report
python -m unittest discover -s tests -v                            # run the test suite
```

`tests/test_report.py` fails if the committed `docs/scenario-report.md` no
longer matches the model, so the generated file never silently drifts from
the assumptions.

## 3D visualizations

`viz/rural-florida-campus.blend` holds three labeled scenes:
`FLRural_Index` (title card and legend), `FLRural_Campus` (elevated
flood-aware campus: grow halls on piers, CUPS-style citrus screenhouse,
packhouse, battery + generator shed, rain tanks and treatment skid, solar
field, retention pond) and `FLRural_Systems` (node-link schematic of water,
power, controls, N+1 and storm mode). Renders are in `viz/renders/`.
Metric units: 1 Blender unit = 1 metre.

## Borrowed from the ai-robot-parenting pattern

- A labeled side scenario beside a baseline, never replacing it.
- Config-driven assumptions; regenerate outputs instead of hand-editing.
- A generated report pinned by tests (report/model agreement enforced).
- Local-first control: the facility keeps running safely without internet.
- N+1 redundancy for pumps, controllers, dosing and the critical power path.
- A qualification ladder: simulated day → wet test → commissioning → first
  crop-cycle audit. Demonstrations are never promoted to dependable capability.
- Honest negatives printed instead of hidden — for example, the placeholder
  battery falls short of the 12-hour critical-load autonomy target, and the
  report says so rather than resizing silently.

## Honesty rules

Same as the baseline: this is concept visualization and placeholder
arithmetic. Real deployment needs site selection, soil and water-table
studies, wind and flood design to real codes, permits, water rights, market
research, food-safety plans and local agronomy.