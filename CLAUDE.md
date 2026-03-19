# Toaster Chef Mobile — Project Context

## What This Is
Toaster Chef is a 3D multiplayer mobile-first game (iOS + Android) and social simulation. Players are Toaster Chefs riding electric trikes equipped with toasters, serving pastries on behalf of a non-profit Kitchen Garage to fight hunger, poverty, and food insecurity. The game models how food, nutrition, and philanthropy create cascading positive change in a community.

## Engine & Platform
- **Engine**: Unity (C#)
- **Target**: Mobile-first — iOS + Android
- **Camera**: Orthographic, locked angles — top-down (fleet/RTS view), three-quarter (~60°, street-level action), isometric (cinematic/reveal)
- **Models**: Meshy AI-generated pre-rigged FBX/GLB models for POC phase

## Multiplayer
- **Photon Fusion 2** — server-authoritative, mobile-optimized, free tier (100 CCU)

## Model Pipeline
Meshy.ai → export FBX or GLB → import Unity → apply Humanoid avatar → Mixamo or Unity animations

## Camera Strategy
- Top-down (90°): fleet management, route assignment (RTS layer)
- Three-quarter (60°): direct pilot control, serving, hawking, NPC interaction
- Isometric (45°): neighborhood reveal, cinematic moments
- All orthographic — no perspective distortion

## Reference
- Original web POC (Phaser 3 + Colyseus): https://github.com/kevinwcrump/toasterchef
- Full game design doc in memory: /Users/kevincrump/.claude/projects/-Users-kevincrump-source/memory/project_toaster_chef.md

## Key Design Principles
- Non-profit model — success measured in meals served, hunger reduced, Community Trust built
- Three core resources: Money, Food, Community Trust
- NPC life states (Housed/Unhoused, Employed/Unemployed) shift based on food access over time
- Staff hired in part from houseless and previously incarcerated NPCs
- Career ladder: Day Laborer → Chef / Mechanic / Pilot → Senior roles
- Delight & Disgust spread through neighborhoods, affecting Appeal Score
- Crime system: prevention (Watch), response (Cops), healing (RJ Circles / Therapy)

## Starting Loadout
1 Kitchen, 1 Chef, 1 Pilot, 1 Trike — limited Money, Food, Community Trust

## Map Tiers
- Tier 1: Corner / Trailer Park (small, intimate)
- Tier 2: Suburb / Small Town (spread out, needs fleet)
- Tier 3: Urban (dense, multiple garages, full simulation)
