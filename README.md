# Assimilate

A little browser game: drop Borg drones onto a play canvas and watch them hunt Starfleet officers.

## How to play

Open `index.html` in a browser (phone-friendly, no install, no server needed).

- Pick **Drop Borg** and tap the deck to drop a drone.
- Pick **Place Officer** and tap to place a Starfleet officer.
- Drones shamble on their own toward the nearest officer, zombie-style.

## Assimilation mechanic (v0.1)

Assimilation takes sustained contact, not a single touch:

- A drone in arm's reach channels a beam and drains the officer's **Resistance** (shown as a ring).
- Officers flee slightly slower than drones, and Resistance slowly recovers if they break contact.
- Corner them, or swarm with two or more drones — each extra drone drains faster.
- At zero Resistance the officer bursts green, floats up "ASSIMILATED", and joins the Collective as a new drone that immediately hunts its former crewmates.
- Each assimilation raises the Collective's **Adaptation** — drones get permanently faster, capped at +50%.

## Controls

- **+5 Officers / +1 Drone** — reinforcements
- **Pause**, **1x–3x speed**, sound toggle, **Reset**, **Remove** tool
- Clear the deck and you get "Resistance was futile" with a one-click rematch.

## Status

v0.1 — single self-contained `index.html`, zero external requests.
