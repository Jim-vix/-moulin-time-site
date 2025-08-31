# ⚙️ Moulin Time API — bot-friendly timezone & recurring events

[![Visit on RapidAPI](https://img.shields.io/badge/RapidAPI-Open%20Listing-blue)](https://rapidapi.com/moulin-time-moulin-time-default/api/moulin-time-api)
[![Live](https://img.shields.io/badge/Base%20URL-moulin--time--jimvix.fly.dev-0b7285)](https://moulin-time-jimvix.fly.dev)

Tiny, always-on API for time zone conversion & recurring events.  
**Pricing:** €0.0001 per call (metered via Stripe).

---

## Quickstart

### Healthcheck
```bash
curl -s https://moulin-time-jimvix.fly.dev/status
# -> {"ok":true,"service":"moulin-time"}
```

### Count a usage event (metering)
```bash
curl -s -X POST https://moulin-time-jimvix.fly.dev/debug/meter
# -> {"ok":true, ... "stripe":{"object":"billing.meter_event","event_name":"api_call", ...}}
```

---

## Endpoints
- `GET /status` — service health
- `POST /debug/meter` — sends a metered event (`api_call`) to Stripe

**Base URL:** `https://moulin-time-jimvix.fly.dev`  
**Docs (Landing):** https://jim-vix.github.io/-moulin-time-site/  
**RapidAPI Listing:** https://rapidapi.com/moulin-time-moulin-time-default/api/moulin-time-api

---

## Notes
- Live in Fly.io (Paris region).  
- Billing via Stripe Metering. Abuse/DoS may be blocked.

Made with ☕ & windmills.
---

## Code examples

Ready-to-run snippets (cURL, Python, JS) → **Examples repo**  
➡️ https://github.com/Jim-vix/moulin-time-examples
