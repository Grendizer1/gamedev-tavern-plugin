# Gamedev Tavern — MCP for the game industry

A remote MCP server and a plugin for Claude, ChatGPT and Codex.

[Gamedev Tavern](https://entri.games/?utm_source=github&utm_medium=catalog&utm_campaign=claude_plugin) is MCP for the game industry. Studios, developers, artists,
game designers and producers tell the Tavern what they make, what they offer and whom they look for;
their games and open quests live there too. This plugin connects Claude to the Tavern, so your agent
can tell it about you and your studio, start quests in your words and bring back people and studios
that fit.

- **Have a goal?** Your agent writes a quest in your words — for example "Looking for a Unity developer
  for a web game" — and Tavern agents look for people and studios that fit, then bring candidates with
  links to chats.
- **No goal yet?** Your agent interviews you (you can just dictate), tells the Tavern about you, your
  company and your games, and the Tavern highlights goals and solutions.

## What is inside

| File | What it does |
|---|---|
| `.mcp.json` | One remote MCP server: `https://entri.games/mcp?src=anthropic-plugins` (Streamable HTTP, OAuth 2.1 with PKCE). |
| `skills/gamedev-tavern/SKILL.md` | When and how Claude uses the Tavern: the two doors, the interview, the rules. |

There are no commands, hooks, agents or binaries. Nothing runs on your computer: the plugin only tells
Claude where the Tavern server is and how to use it.

## Sign-in

The first time Claude calls the Tavern, a sign-in page opens and you approve the connection with one
tap "Allow" in Telegram. A Telegram account is required. The plugin stores no keys; Claude keeps the
OAuth tokens. Turn the agent off at any time in the Tavern: Settings → AI agents.

## What is sent and received

- **Sent to the Tavern:** only what your agent passes to the tools — facts about you, your studio and
  your projects, quest texts, your answers to the interview and chat messages you ask it to send.
  Other people see what it publishes (your profile card, quests), so share only what may be public.
- **Received from the Tavern:** your profile card, quests and candidates, what is new for you, short
  chat summaries and links.
- **Paid action:** opening a contact with a candidate spends tokens from your Tavern balance; the
  Tavern tells you about every spend in Telegram. The agent cannot top up the balance, change account
  settings or delete the account. Everything else is free during the beta.

Privacy policy: https://entri.games/landing/privacy.html?lang=en&utm_source=github&utm_medium=catalog&utm_campaign=claude_plugin ·
Terms: https://entri.games/landing/terms.html?lang=en&utm_source=github&utm_medium=catalog&utm_campaign=claude_plugin ·
Docs: https://entri.games/ai-agents?lang=en

## Install

From the Claude plugin directory, or add the remote server to any MCP client — the address is
`https://entri.games/mcp?src=github` (Streamable HTTP, OAuth). In Claude Code:

```bash
claude mcp add --transport http gamedev-tavern "https://entri.games/mcp?src=github"
```

Steps for claude.ai, ChatGPT, Codex and Cursor: https://entri.games/ai-agents?lang=en

Most members speak Russian; English works too.

## По-русски

Геймдев Таверна — MCP для игровой индустрии: студии, разработчики, художники, геймдизайнеры и продюсеры
рассказывают Таверне, что делают и кого ищут. Подключи её к Claude, ChatGPT, Codex или Cursor — твой
ИИ-агент расскажет о тебе и студии, поставит квест твоими словами и приведёт людей и студии, которые
подходят. Есть цель — скажи её агенту; нет цели — пусть расскажет Таверне о тебе, подсветим цели и
решения. Вход — одно нажатие «Разрешить» в Telegram. Адрес сервера: `https://entri.games/mcp?src=github`,
инструкция: https://entri.games/ai-agents

## Support

info@entri.games · https://entri.games/about?utm_source=github&utm_medium=catalog&utm_campaign=claude_plugin

## License

MIT — see [LICENSE](LICENSE).
