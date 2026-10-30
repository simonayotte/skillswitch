# skill-toggle

Turn agent skills on and off for every coding agent at once (Claude Code, Codex, OpenCode, Cursor, Pi, …).

It works on the shared skills folder (`~/.agents/skills`): a skill is off when its `SKILL.md` is renamed to `SKILL.md.disabled`, so no agent loads it.

## Install

Requires `zsh` and `fzf`.

```sh
ln -s "$PWD/skills" ~/.local/bin/skills
```

## Usage

```sh
skills                  # picker: jk move · hl page · space toggle · q quit
skills ls               # list groups and skills with their state
skills off ui           # turn off a group (or "@ui")
skills on better-ui how # turn on skills
```

● on · ● off · ● group partly on. Toggling a group turns all its skills on, or all off when they're already all on.

## Groups

Define groups in `~/.agents/skill-groups`, one per line, with skill names or globs:

```
ui: animate* better-* apple-design
```

Override paths with `SKILLS_DIR` and `SKILLS_GROUPS`.
