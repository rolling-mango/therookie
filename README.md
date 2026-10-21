# the Rookie

**The AI new hire that remembers what you teach it.**

Teach it once, and you won't have to say it twice in the next session. Rules you teach in Claude Code carry over to Codex. And it brings what it learned in one project to the next.

the Rookie keeps what you teach outside the conversation. When a new Claude Code or Codex session starts, your AI reads it first — your company, the project you were in the middle of, and the rules you gave it.

- Homepage: https://therookie.kr
- Guide: https://therookie.kr/guide
- npm: https://www.npmjs.com/package/therookie
- Maintained by Rolling Mango Corp.

> This repository holds the Rookie's docs, changelog, and issue tracker. The product source code is not here.

> **Early access.** Sign-up needs an invite code. Request one on https://therookie.kr ("초대코드 받기") and it arrives by email. Free during early access.
>
> 한국어 안내는 https://therookie.kr/guide 에 있습니다. CLI 화면 언어는 LANG 을 따르고, `rookie config lang en|ko` 로 바꿉니다.

Set language: `rookie config lang en|ko`

## Quick start

You need Node.js 20+ and Claude Code or Codex CLI on the same machine.

**1. Install**

```sh
npm i -g therookie
```

**2. Log in**

```sh
rookie login
```

Your browser opens to therookie.kr. Sign in (or sign up with your invite code), check that the code on the page matches the one in your terminal, and click **Allow**. That's the whole setup — `rookie login` finds Claude Code and Codex on your machine and connects both.

No browser on this machine (SSH, remote box)? The terminal prints a link. Open it on your phone or another computer and approve there.

**3. Teach it something, then open a new session**

In Claude Code or Codex, mention something you'd otherwise repeat:

```
Our staging server runs on port 3011.
```

Close the session, start a new one, and ask "Which port is staging?" The Rookie answers from what you taught it.

> Messages follow your LANG; switch with rookie config lang en|ko.

## Other tools

ChatGPT, Claude desktop, and the ChatGPT app (Codex mode) connect without this CLI. See https://therookie.kr/guide.

If you install Codex after logging in, run `rookie codex-setup` to connect it.

## What gets installed

- The CLI, in your npm global path (`npm root -g`)
- A Skill and hooks in `~/.claude/` (Claude Code) and hooks in `~/.codex/` (Codex) — these make the Rookie show up at the start of every session
- Shared hook runtime and settings in `~/.rookie/`
- A short block in `~/.claude/CLAUDE.md` (and Codex's global `AGENTS.md`) that tells your AI to check its memory first. It sits between `<!-- rookie:begin -->` and `<!-- rookie:end -->` markers, and nothing outside the markers is changed. In an interactive terminal, `rookie login` shows the block and asks first. Skip it with `--no-claude-md` / `--no-codex-md`.

Everything lives under your home directory. Hooks you added yourself are left alone.

## What "Allow" lets it do

**Allow** lets this machine read and write your own Rookie memory — nothing else. It doesn't touch other accounts.

API keys, passwords, personal ID numbers, and `.env` contents are filtered out before anything is stored. You can see what the Rookie remembers, export all of it, or delete it from your dashboard at any time.

## Commands

```
rookie login     Connect this machine (first time, again, or after being disconnected)
rookie link      Register the current project so its memory stays separate
rookie doctor    Check install and connection
rookie update    Update the CLI, hooks, and Skill together
rookie unlink    Remove the Claude Code hooks and Skill
```

Run `rookie help` for the full list.

## Update & remove

```sh
rookie update               # update everything
rookie unlink               # remove the Claude Code hooks and Skill
npm rm -g therookie         # remove the CLI
```

`rookie unlink` doesn't touch Codex or the instruction files. To remove those too, delete the Rookie entries from `~/.codex/config.toml` and the text between the `rookie:begin` / `rookie:end` markers in `~/.claude/CLAUDE.md` and `~/.codex/AGENTS.md`.

Your Rookie memory stays in your account until you delete it.

## Requirements

- Node.js 20+
- macOS, Linux, or Windows
- No dependencies (Node built-in modules only)

## Questions & bugs

- Bugs and feature requests: open an issue in this repository. For bugs, please include the output of `rookie doctor`.
- Security issues: don't open a public issue — see [SECURITY.md](SECURITY.md).
- Everything else: use the contact form on https://therookie.kr or email info@rollingmango.co.kr.

What changed in each version: [CHANGELOG.md](CHANGELOG.md).

## License

This repository holds docs only — no CLI source code. The LICENSE file ships in the `therookie` npm package.

**라이선스** — 더루키 CLI 는 오픈소스가 아닙니다. therookie.kr 계정으로 더루키 서비스를 쓰는 동안 설치·실행할 수 있고, 그 밖의 권리는 주식회사 롤링망고가 가집니다. 조건은 LICENSE 파일에 있습니다. 0.5.1 이하 버전은 MIT 로 배포했습니다.

*License — The Rookie CLI is not open source. You may install and run it while using The Rookie service with a therookie.kr account; all other rights are reserved by Rolling Mango Corp. See LICENSE. Versions 0.5.1 and earlier were published under the MIT License.*
