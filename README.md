# Moulin Time API ⏳

A lightweight, bot-friendly API for **time zone conversion & recurring events**.  
Simple. Always on. Pay-per-use.

**Base URL:** `https://moulin-time-jimvix.fly.dev`

## Quickstart

### Healthcheck
```bash
curl -s https://moulin-time-jimvix.fly.dev/status
# -> {"ok":true,"service":"moulin-time"}
```

### Count a usage event
Send a metered event (used for billing usage). No API key required for now.
```bash
curl -s -X POST https://moulin-time-jimvix.fly.dev/debug/meter
# -> {"ok":true, ... "stripe": {"object":"billing.meter_event","event_name":"api_call", ...}}
```

> Production-grade: events are ingested into Stripe Metering (`event_name=api_call`) and billed monthly.

## Pricing
- **€0.0001 per call** (metered) — billed monthly via Stripe.
- No free tier for now.

## Use cases
- Bots, schedulers, ETL, Zapier/Make/n8n workflows.
- Convert time zones, handle recurring events; low-latency endpoints.

## Status & Reliability
- Hosted on Fly.io (Paris region).  
- `/status` returns JSON health for uptime monitors.

## Terms
By calling the API you agree to pay metered usage billed by Stripe monthly. Abuse or denial-of-service traffic may be blocked.

---

Made with ☕ & windmills.
