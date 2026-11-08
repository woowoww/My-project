# AI Fruit Motivational Video Studio

A six-role team for making short, inspirational fruit videos (30–45 seconds, vertical 9:16).

## Team

| Role | Sub-agent | Output file |
|---|---|---|
| Writer | `studio-writer` | `01-writing.md` |
| Story Writer | `studio-story-writer` | `02-story.md` |
| Set Designer (scene set-up) | `studio-set-designer` | `03-scenes.md` |
| Camera Operator | `studio-camera` | `04-shots.md` |
| Director | `studio-director` | `05-direction.md` |
| Producer | `studio-producer` | `06-production.md` |

Agent definitions live in `.claude/agents/`.

## Pipeline

1. **Writer** writes hooks, voiceover and captions for a theme.
2. **Story Writer** builds the beat arc around the voiceover.
3. **Set Designer** builds each scene's world.
4. **Camera Operator** plans the shots.
5. **Director** reviews 01–04 and returns `APPROVED` or `REVISE`. Revisions loop back to the owning role.
6. **Producer** builds the production package once approved. Publishing needs the user's explicit go-ahead.

## Shared files

- `studio/bible.md`: characters, signature colours, tone, banned claims. Every role reads this first.
- `studio/episodes/<episode-id>/`: one folder per episode, holding the six output files.

## Standing rules

- Motivation comes from a small, real action by a fruit character, never from shame or a lecture.
- No health, money, or guaranteed-outcome claims.
- Keep the visual style consistent across episodes.
- The `fruit-drama-video` skill has its own locked style for the "Avocado's Rock Bottom" series. Do not mix that style into this studio unless the user asks.
