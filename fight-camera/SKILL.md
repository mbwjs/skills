---
name: "fight-camera"
description: "High-speed fight cinematography camera language for video generation prompts: one-take camera moves, speed tiers (swift/whip/gentle/shock), and shot-size pairings for martial arts and action scenes. Use when the user asks for fight, combat, martial-arts, or action-fight video prompts, or says 高速打斗 / 打斗运镜."
metadata: { "includeInPrompt": true }
---

# Fight Camera

## Purpose
Apply the user's 万能高速打斗运镜手册 camera language to video generation prompts for fight/combat scenes. The camera follows the action trajectory, amplifies attack direction and force, and manufactures speed through lens movement. The full manual lives in `references/fight-camera-manual.md`; this file carries the operating core only.

## Workflow
1. Confirm the scene is a fight/action sequence. If it is not, do not apply this skill.
2. Break the fight into action beats (起手对冲 / 腿法连击 / 闪避错位 / 魔物反击 / 命中破防 / 尾帧蓄力).
3. For each beat, pick from `references/fight-camera-manual.md`:
   - a 机位调度 formula (one of the 10: 起手冲刺, 高速错位, 腿法轨迹, 腾空动作, 命中瞬间, 被震飞, 追击连招, 魔物反击, 高空压制, 尾帧连招前摇),
   - a 速度档位 (Swift / Whip / Gentle / Shock),
   - a 景别 (FS / MS / CU / MCU / 仰拍 / 反向).
4. Copy the chosen 万能写法 verbatim into the prompt (see Operating Rules).
5. Verify against the total mantra before delivering: 低机位冲，贴地跟；环绕错，甩镜追；特写打，震动停；后拉开，尾帧续。

## Output Contract
- The user's original prompt text passes through to the generation tool verbatim, unmodified.
- Camera language from this skill is appended as separate camera-direction blocks, one per action beat, in beat order.
- Each block states: 景别 + 运镜方式 + 速度档位 + 明确目的 (让观众看清动作轨迹 / 强化攻击方向和力量 / 用镜头速度制造压迫感).

## Operating Rules
1. Never rewrite, expand, summarize, or translate the user's prompt. Append camera blocks only.
2. One continuous take per sequence: no hard cuts unless the user asks for them.
3. Every camera move must have an explicit target (追随动作轨迹 / 跟随攻击方向 / 锁定命中点). No unmotivated rotation or free-floating game camera.
4. 命中瞬间 must include a brief hold: 0.15 秒凝滞锐化, then shock vibration, then resume motion.
5. 尾帧 must not freeze on a pose; end on the pre-attack蓄力 moment: MCU 中近景 + PULL gentle, leaving room for the next strike.
6. When the user supplies their own camera wording, theirs wins; this manual only fills what they didn't specify.
