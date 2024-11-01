# drg-mission-gen
Info formatter for Deep Rock Galactic's weekly Deep Dives. 

Seeds are taken from `https://drg.ghostship.dk/events/deepdive` and automatically fetched via [AssemblyStorm](https://github.com/trumank)'s [GSG Endpoint CLI](https://github.com/trumank/drg-mission-gen/tree/master/drg_mission_gen_gsg_endpoint_cli) (implemented by [memtransmute](https://github.com/jieyouxu)).

## Usage
### Example input `--format=plain`

`$ cargo run --bin drg_mission_gen_gsg_endpoint_cli -- --format=plain`

Example output:
```
=== Deep Dive Info ===
Start: 2024-07-11
End: 2024-07-18
Seed: 3422115630

=== Normal Deep Dive ===
Codename: Unknown Comeback
Biome: Azure Weald

+-------+------------------+--------------------------+----------------+-------------------+
| Stage | Primary          | Secondary                | Warning        | Mutator           |
+-------+------------------+--------------------------+----------------+-------------------+
| 1     | 250 Morkite      | Kill 1 Dreadnought       | Parasites      |                   |
+-------+------------------+--------------------------+----------------+-------------------+
| 2     | 6 Eggs           | Repair 2 Mini-M.U.L.E.s  | Mactera Plague |                   |
+-------+------------------+--------------------------+----------------+-------------------+
| 3     | 3 Mini-M.U.L.E.s | 2 Resonance Crystals     |                | Critical Weakness |
+-------+------------------+--------------------------+----------------+-------------------+


=== Elite Deep Dive ===
Codename: Clean Bed
Biome: Sandblasted Corridors

+-------+------------------+-----------------------+----------------+-----------------+
| Stage | Primary          | Secondary             | Warning        | Mutator         |
+-------+------------------+-----------------------+----------------+-----------------+
| 1     | On-Site Refining | 2 Resonance Crystals  | Duck and Cover |                 |
+-------+------------------+-----------------------+----------------+-----------------+
| 2     | Escort Duty      | Liquid Morkite Well   | Swarmageddon   |                 |
+-------+------------------+-----------------------+----------------+-----------------+
| 3     | On-Site Refining | Collect 150 Morkite   | Lethal Enemies | Rich Atmosphere |
+-------+------------------+-----------------------+----------------+-----------------+
```

### Example input `--format=discord`

`$ cargo run --bin drg_mission_gen_gsg_endpoint_cli -- --format=discord`

Example output:
```
Weekly Deep Dives information for **2024-07-11 to 2024-07-18**.
Deep Dives will reset <t:1721300400:F>

:Deep_Dive: __**DEEP DIVE**__ :Deep_Dive:
Region: **Azure Weald** | Code Name: **Unknown Comeback**
Stage 1: **:morkite: 250 Morkite** + **:dreadegg: Dreadnought** | :tothebone: **Parasites**
Stage 2: **:gegg: 6 Eggs** + **:molly: Repair 2 Mini-M.U.L.E.s** | :tothebone: **Mactera Plague**
Stage 3: **:molly: 3 Mini-M.U.L.E.s** + **:pingdrg: 2 Resonance Crystals** | :rocknstone: **Critical Weakness**

:Deep_Dive: __**ELITE DEEP DIVE**__ :Deep_Dive:
Region: **Sandblasted Corridors** | Code Name: **Clean Bed**
Stage 1: **:refinerywell: On-Site Refining** + **:pingdrg: 2 Resonance Crystals** | :tothebone: **Duck and Cover**
Stage 2: **:drill: Escort Duty** + **:refinerywell: Liquid Morkite Well** | :tothebone: **Swarmageddon**
Stage 3: **:refinerywell: On-Site Refining** + **:morkite: 150 Morkite** | :rocknstone: **Rich Atmosphere** :tothebone: **Lethal Enemies**
```
![image](https://github.com/user-attachments/assets/5b05748c-05a9-4293-8e40-350a1de34594)

## Known Issues
  - The variety of Dreadnought required on Elimination objectives is not fetched.
