# Assimilate

A little browser game: drop Borg drones onto a play canvas and watch them hunt Starfleet officers.

## How to play

Open `index.html` in a browser (phone-friendly, no install, no server needed).

- Pick **Drop Borg** and tap the deck to drop a drone.
- Pick **Place Officer** and tap to place a Starfleet officer.
- Drones shamble on their own toward the nearest officer, zombie-style.

## Level design (v0.3)

The Borg beam aboard a Starfleet ship. The playfield is a deck plan, not an open floor:

- **Transporter Room** (top-left) — Borg beam in here on reset, glowing pads.
- Six labelled rooms — **Bridge** (viewscreen), **Science Lab**, **Cargo Bay** (crates), **Engineering** (pulsing warp core), **Sickbay** (biobeds) — linked by a lit central corridor.
- Bulkheads are real walls: they block movement and phaser fire. Drones pathfind doorway-to-doorway, officers flee room to room. Clicking a bulkhead refuses placement with a "BULKHEAD" tag.

## Assimilation mechanic

Assimilation takes sustained contact, not a single touch:

- A drone in arm's reach channels a beam and drains the officer's **Resistance** (shown as a ring).
- Officers flee slightly slower than drones, and Resistance slowly recovers if they break contact.
- Corner them, or swarm with two or more drones — each extra drone drains faster.
- At zero Resistance the officer bursts green, floats up "ASSIMILATED", and joins the Collective as a new drone that immediately hunts its former crewmates.
- Each assimilation raises the Collective's **Adaptation** — drones get permanently faster, capped at +50%.

## Phasers and adaptive shields (v0.2)

Officers shoot back, with a different phaser per class:

- **Command (red)** — heavy, slow Type III rifle
- **Operations (gold)** — balanced Type II
- **Science (teal)** — weak but fast Type I

Each phaser sits on one of four frequencies. After 3 landed hits on one frequency the Borg adapt — the shield bubble flares, an "ADAPTED" tag appears, and that frequency is neutralised until the officer remodulates (~6 s). Only **Captains** (four pips, gold ring) carry the adaptive phaser, which rotates frequency every shot so it can never be adapted to. Captain shots do not count toward adaptation.

Drones have 260 HP with a health bar; destroyed drones are counted, and losing all drones shows "The Collective has been destroyed". Bulkhead clicks refuse placement with a "BULKHEAD" tag — units can never be placed inside a wall.

## Controls

- **+5 Officers / +1 Drone** — reinforcements
- **Pause**, **1x–3x speed**, sound toggle, **Reset**, **Remove** tool
- Clear the deck and you get "Resistance was futile" with a one-click rematch.

## Status

v0.3 — single self-contained `index.html`, zero external requests.
