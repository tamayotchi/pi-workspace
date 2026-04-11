# Pi workspace

This folder is the source of truth for your Pi customization setup.

## What is wired here

- `settings.json` -> your global Pi settings (symlinked from `~/.pi/agent/settings.json`)
- `package.json` -> local Pi package manifest
- `extensions/` -> your custom extensions
- `themes/` -> your custom themes / UI colors
- `skills/` -> your custom skills
- `prompts/` -> your prompt templates

## How Pi loads this folder

Your global settings include this folder as a local Pi package:

- `/home/tamayotchi/pi-workspace`

That means Pi reads resources directly from here without copying them anywhere else.

## Editing flow

- Change `settings.json` here -> Pi global config changes too
- Change files in `extensions/`, `skills/`, or `prompts/` -> run `/reload` in Pi
- Change the active custom theme in `themes/` -> Pi should hot-reload it when that theme is active

## Included now

- `themes/workspace-dark.json` -> optional custom theme example

## Notes

- Auth stays in `~/.pi/agent/auth.json`
- Sessions stay in `~/.pi/agent/sessions`
- Safe to git-init this folder if you want to version your custom Pi setup
