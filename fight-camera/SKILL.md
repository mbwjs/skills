---
name: "fight-camera"
description: "High-speed fight cinematography camera language for video generation prompts: one-take camera moves, speed tiers (swift/whip/gentle/shock), and shot-size pairings for martial arts and action scenes. Use when the user asks for fight, combat, martial-arts, or action-fight video prompts."
metadata: { "includeInPrompt": true }
---

# Fight Camera

## Purpose
Apply the Universal High-Speed Fight Cinematography Manual's camera language to video generation prompts for fight/combat scenes. The camera follows the action trajectory, amplifies attack direction and force, and manufactures speed through lens movement. The full manual lives in `references/fight-camera-manual.md`; this file carries the operating core only.

## Workflow
1. Confirm the scene is a fight/action sequence. If it is not, do not apply this skill.
2. Break the fight into action beats (opening clash / kick combo / dodge crossover / monster counterattack / impact breakthrough / end-frame wind-up).
3. For each beat, pick from `references/fight-camera-manual.md`:
   - a camera formula (one of the 10: Opening Charge, High-Speed Crossover, Kick Trajectory, Aerial Move, Impact Moment, Knockback, Pursuit Combo, Monster Counterattack, Overhead Suppression, End-Frame Combo Wind-Up),
   - a speed tier (Swift / Whip / Gentle / Shock),
   - a shot size (FS / MS / CU / MCU / low-angle / reverse).
4. Copy the chosen universal wording verbatim into the prompt (see Operating Rules).
5. Verify against the total mantra before delivering: "Low angle charge, track low to the ground; orbit the cross, whip-pan the chase; punch in close, freeze-shake on impact; pull back wide, end on the wind-up."

## Output Contract
- The user's original prompt text passes through to the generation tool verbatim, unmodified.
- Camera language from this skill is appended as separate camera-direction blocks, one per action beat, in beat order.
- Each block states: shot size + camera move + speed tier + explicit purpose (let the viewer read the action trajectory / amplify attack direction and force / manufacture pressure through lens speed).

## Operating Rules
1. Never rewrite, expand, summarize, or translate the user's prompt. Append camera blocks only.
2. One continuous take per sequence: no hard cuts unless the user asks for them.
3. Every camera move must have an explicit target (follow the action trajectory / follow the attack direction / lock onto the impact point). No unmotivated rotation or free-floating game camera.
4. The impact moment must include a brief hold: 0.15-second freeze-sharpen, then shock vibration, then resume motion.
5. The end frame must not freeze on a pose; end on the pre-attack wind-up moment: MCU medium close-up + PULL gentle, leaving room for the next strike.
6. When the user supplies their own camera wording, theirs wins; this manual only fills what they didn't specify.
