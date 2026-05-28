# ai4HomeReno
how i AI to manage house rebuild projects
Complete electrical procurement documentation for the renovation at 1176 Greenwood Ave, Palo Alto CA 94301.
Covers the full workflow from contractor quote review → product selection → compatibility validation → cart audit → final electrician install guide.

# Electrical Procurement
 
Complete electrical procurement documentation for the renovation at **1176 Greenwood Ave, Palo Alto CA 94301**.
 
Covers the full workflow from contractor quote review → product selection → compatibility validation → cart audit → final electrician install guide.

## Files in This Repo
 
| File | Description |
|---|---|
| `README.md` | This file — project overview and procurement summary |
| `electrician_guide.pdf` | Room-by-room install guide for the electrician |
| `home-procurement-skill.skill` | Reusable Claude skill for future procurement projects |
| `home-procurement-README.md` | Documentation for the procurement skill |

---
 
## Design Strategy
 
The original contractor quote used standard Leviton Decora devices throughout. This project upgraded to a **Legrand hybrid collection** strategy:
 
- **Legrand adorne** — showstopper 4-gang clusters (living room, entryway, kitchen) for premium aesthetics
- **Legrand radiant** — all other locations for consistent matte white decorator finish
- **Pass & Seymour** — humidity sensor switches (fan + light combo) for bathrooms, laundry, and utility room
- **Retained Leviton** — 30A appliance outlet (no Legrand radiant 30A equivalent exists)
Wall color reference: Sherwin Williams SW 7101 Futon (warm charcoal). Kitchen countertop: Essenza MA01 Terrazzo White matte slab.

## Procurement Workflow
 
This project was managed using a custom Claude skill (`home-procurement-skill.skill`) that encodes:
 
1. Intake — reading contractor quotes and cart PDFs
2. Product recommendation with compatibility validation
3. Cart audit with status flags (correct / verify / wrong item / missing)
4. Location-based decision framework (amperage by room, sensor placement)
5. Final order summary table
6. Action item tracking
7. Cross-AI validation to prevent hallucinated product numbers
See `home-procurement-README.md` for installation and usage instructions.
 
---
 
## Notes for Electrician
 
- Full room-by-room install guide with model numbers and quantities: see `electrician_guide.pdf`
- adorne showstopper clusters: **all 4 devices per plate must be adorne** — no radiant substitutions
- HSWC3W humidity sensors fit NEMA WD6 openings in radiant plates — compatible despite different brand
- Smoke detectors: wire all 6 Innolink units on the same interconnect chain before connecting to any non-Innolink units
- 30A outlet (R10-00278-S00): dedicated circuit, paired with Leviton SS plate (R50-SL703-000)
