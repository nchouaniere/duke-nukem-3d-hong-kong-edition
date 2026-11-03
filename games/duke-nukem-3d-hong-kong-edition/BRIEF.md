# Duke Nukem 3D Hong Kong edition

STORY
In this fictional action-game setting, a radical faction of student activists has escalated demonstrations into sabotage, attacks on infrastructure, and dangerous street confrontations. Most students and residents are civilians; some oppose the faction, some support its cause peacefully, and many are simply caught in the crisis.

A fictional government liaison sends Duke Nukem to protect civilians, prevent further damage, and restore order. Duke’s objectives are to disarm hazards, secure critical sites, rescue people, and stop the faction’s leaders from carrying out a citywide plan—not to attack people for their political beliefs.

Keep the faction and events fictional. Do not portray real student groups, political organizations, or peaceful protesters as terrorists or enemies. Include choices that favor de-escalation and civilian safety, alongside action against armed saboteurs.

---

## The JumPHP playground

This project was made on the JumPHP playground: the game's page is https://jumphp.net/duke-nukem-3d-hong-kong-edition
(category: Tir).

- The game is `games/duke-nukem-3d-hong-kong-edition/`. Read `AGENTS.md` (the JumPHP contract) first; replace the skeleton with the game
  described above; follow the definition of done (tests, screenshots you look at, browser build).
- **Develop with game tests, visually**: for each mechanic, as you write it, a test in `games/duke-nukem-3d-hong-kong-edition/tests/` that
  extends `JumPHP\Testing\GameTestCase` and plays it ("the player jumps onto the platform", "the enemy dies
  when hit"; AGENTS.md "Game tests"); `bin/jumphp test duke-nukem-3d-hong-kong-edition` after each change. The user watches them play live
  in Claude Code (the `jumphp-live` pane) and, after a push, replays each test filmed in the studio (MCP
  `run_tests`).
- **Publishing**: every push to `main` is online within a minute (GitHub webhook). The MCP tool
  `sync_project` (server `jumphp`) publishes at once and returns the errors: a commit with a PHP syntax error
  is not published (the previous version stays online).
- The playground loads the game file by file with its shared engine: Composer packages other than
  `jumphp/engine` are not available there.
- **The game's home page**: make `games/duke-nukem-3d-hong-kong-edition/site/` (AGENTS.md section 13: themed with the game's own graphics,
  SEO, a link to `play/`); it is the game's page on the playground. Also `games/duke-nukem-3d-hong-kong-edition/assets/thumbnail.png`.
- When the game is done: MCP `update_project` with `listed: true` shows it in the playground's directory.