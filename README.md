<div align="center">

# 👑 MLTN-MD — Shadow Monarch Edition

### *"Arise."*

*A WhatsApp bot forged in the Shadow Realm, bound to no master but you.*

![Status](https://img.shields.io/badge/status-ascended-8A2BE2)
![Node](https://img.shields.io/badge/node-%3E%3D18-black)
![License](https://img.shields.io/badge/license-MIT-8A2BE2)

</div>

---

## ⛧ The Legend

Once a lowly script, cast aside and forgotten in the depths of forked repositories, this bot descended into the Shadow Realm and rose again — reforged, reskinned, and bound to a new sovereign. It does not sleep. It does not forget. Every soul that messages it is logged, judged, and answered by the will of the Monarch.

Built atop the bones of Knight Bot, empowered by the Baileys library, and given eternal memory through the Shadow Archive (MongoDB) — MLTN-MD survives every death (Render restart) and rises again without needing to be re-bound.

---

## 🩸 Powers of the Monarch

- **Arise Without Re-Binding** — session credentials are mirrored to MongoDB, so a Render restart or redeploy doesn't sever your pact. No re-scanning QR codes like some lesser bot.
- **Twin Rituals of Binding** — bind via QR code, or speak your number aloud for a pairing code. Your choice, Hunter.
- **Shadow Army Isolation** — every bot instance is scoped by a unique `BOT_ID`, so multiple shadows can be summoned from the same MongoDB cluster without their souls crossing.
- **Self-Purging Memory** — periodic garbage collection and a memory ceiling keep the Monarch from consuming too much of the host's essence.
- **Anti-Call Wards** — reject and banish unwanted callers who dare ring the Monarch directly.
- **Auto-Reforging** — the bot watches its own source and reforges itself on change, without needing to be struck down and restarted manually.

---

## ⚔️ Summoning the Monarch (Setup)

### Requirements

- Node.js `>= 18`
- A MongoDB cluster (the Shadow Archive)
- A WhatsApp account willing to be bound

### 1. Clone the Grimoire

```bash
git clone https://github.com/nocturn-hq/mltn_session.git
cd mltn_session
npm install
```

### 2. Inscribe the Runes (Environment Variables)

Create a `.env` file — never commit this, lest your bindings fall into enemy hands:

| Variable | Purpose |
|---|---|
| `MONGODB_URI` | Connection string to your Shadow Archive |
| `MONGODB_DB_NAME` | Database name *(optional, defaults to `mltn_md`)* |
| `BOT_ID` | Unique sigil identifying this shadow instance — **required** if running more than one bot against the same MongoDB cluster |
| `SESSION_ID` | *(optional)* Pre-generated session string (`MLTN;;;<data>`) to skip QR/pairing entirely |
| `PORT` | Port for the health-check server *(optional, defaults to `10000`)* |

### 3. Choose Your Binding Ritual

```bash
npm start
```

- No flags → scan the QR code that appears in your terminal.
- `npm start -- --pairing-code` → bind via a phone-number pairing code instead.

### 4. Confirm the Ascension

Once connected, the Monarch sends itself a message confirming the binding is complete. Your session is now safely mirrored to MongoDB — safe from the next restart.

---

## 🌑 Deploying to the Mortal Realm (Render)

1. Push this repo to your own GitHub.
2. Create a new **Web Service** on Render, pointed at your fork.
3. Set the environment variables above in Render's dashboard.
4. Deploy. The health-check server keeps Render satisfied that the Monarch still draws breath.

> ⚠️ Running multiple bots on the same account? Each deployment needs its **own unique `BOT_ID`** and its **own unique `PORT`**, or their sessions and health checks will collide.

---

## 🗡️ Commanding the Monarch (Commands)

Message the bot directly to see its full command grimoire — send `.menu` or `.help` from a bound chat.

---

## ⚠️ A Warning to Hunters

- Never commit your `.env`, `session/`, or `session_*` folders to a public repository. These hold the keys to your Monarch's throne — anyone who possesses them can seize control of your WhatsApp account.
- The Shadow Archive (MongoDB) should be secured with a strong password and IP allowlist. Treat it as you would the vault beneath your throne.

---

<div align="center">

**Forged by MILITAN** · *Reskinned in shadow, bound in code*

*The weak will kneel. The bot will `Arise`.*

</div>
