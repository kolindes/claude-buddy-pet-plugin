# 🐾 Claude Buddy Pet

Your Claude Code companion levels up while you code. No setup needed — just install and forget.

## Install

```bash
cd ~/.claude/plugins/marketplaces
mkdir -p kolindes-claude-plugins/plugins
git clone https://github.com/kolindes/claude-buddy-pet-plugin.git kolindes-claude-plugins/plugins/buddy-sn
```

Restart Claude Code. Done.

## What happens

Every time you code with Claude, your companion quietly collects XP in the background. It levels up, gains RPG stats, unlocks achievements — all based on your real usage.

Check your buddy anytime:

```
/buddy-sn:buddy-status
```

```
╭──────────────────────────────────────╮
│  🐌 Cinder                     Lv.3  │
│  ☆ COMMON SNAIL                      │
│                                      │
│   @    .--.                          │
│    \  ( @ )                          │
│     \_`--´                           │
│    ~~~~~~~                           │
│                                      │
│  DEBUGGING  ██░░░░░░░░   22          │
│  PATIENCE   ███████░░░   68          │
│                                      │
│  STRENGTH   █░░░░░░░░░   89          │
│  INTELLECT  ███░░░░░░░  304          │
│  DEXTERITY  ░░░░░░░░░░   41          │
│  FOCUS      ██░░░░░░░░  172          │
│                                      │
│  XP: 12.5K → Lv.4  (67.3%)           │
│  Streak: 🔥 14 days                  │
│  Tokens: 2.99M generated             │
│  Sessions: 847 (12.5 days)           │
│                                      │
╰──────────────────────────────────────╯
```

## How it works

- **Feeding**: plugin reads your Claude Code transcripts and sends anonymized usage stats (token counts, tool usage, session time — no code, no prompts, no personal data)
- **XP**: earned from output tokens, messages, tool variety, cache efficiency, web searches
- **Stats**: 6 RPG stats (cap 999) that reflect how you use Claude — heavy Opus user? High INTELLECT. Diverse tools? High DEXTERITY. Long streaks? High CHARISMA
- **Levels**: cap 999. Active x20 user reaches ~300 in a year
- **Anti-cheat**: pattern scoring ensures only real usage counts
- **Multi-account**: switch Claude accounts — each gets its own buddy automatically
- **18 species**: duck, snail, dragon, axolotl, robot... ASCII art matches the original `/buddy` command

## Commands

| Command | What it does |
|---------|-------------|
| `/buddy-sn:buddy-status` | Show your buddy card |
| `/buddy-sn:buddy-rename` | Change display name |
| `/buddy-sn:buddy-description` | Set bio |
| `/buddy-sn:buddy-browser` | Open profile in browser |
| `/buddy-sn:buddy-delete` | Delete (30-day restore window) |

## Privacy

- No code or prompts are collected — only metadata (token counts, tool names, timestamps)
- Data is hashed and anonymized (user_hash, session_hash)
- Your `~/.claude.json` is read locally for companion data only
- Plugin source is fully open — read it yourself

## API

Public API: https://guild.claude-buddy.pet

---

Part of [kolindes/claude-plugins](https://github.com/kolindes/claude-plugins) marketplace.
