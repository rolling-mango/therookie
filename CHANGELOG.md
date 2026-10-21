# Changelog

User-facing changes to the `therookie` CLI. Dates are npm publish dates (UTC).

## 0.5.2 — 2026-10-21

- The license changed from MIT to a license to use with The Rookie service. See LICENSE in the npm package. 0.5.1 and earlier stay under MIT.
- English messages are polished, and they point you to web pages by address instead of by screen name.

## 0.5.1 — 2026-10-21

- Wording in messages is made consistent. Nothing works differently.

## 0.5.0 — 2026-10-21

- The CLI can show its messages in English. Switch with `rookie config lang en|ko`.
- If you don't set a language, it follows your LANG.

## 0.4.51 — 2026-10-21

- Development comments are removed from the published files. Nothing works differently.

## 0.4.50 — 2026-10-21

- Rewrote the npm page to match the current install and login steps.

## 0.4.48 — 2026-10-16

- Logging in again cleans up this machine's old connections. If a connection can't be confirmed, it asks you first.
- On a remote machine, you can log in with a single link. When the connection drops, the message tells you why and what to do next.

## 0.4.47 — 2026-10-15

- Task rules load in more situations: when a Skill or tool is called, and when the first line of your message starts with `업무:` (task).
- The rules for the task are added to your first message, trimmed to fit.

## 0.4.46 — 2026-10-15

- Running a build, deploy, database, or operations command loads the rules for that task right away.

## 0.4.45 — 2026-10-14

- Rules you teach for a specific task are loaded when that task starts, and followed.
- `rookie rules <task>` shows the rules for a task.

## 0.4.44 — 2026-10-08

- Write a personality and identity for your Rookie, and it works in that character.
- `rookie update` now updates the CLI itself, too.
