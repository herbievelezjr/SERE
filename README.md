# SERE — Survive, Evade, Resist, Escape

**A sandboxed cybersecurity training-simulation concept.**
Version 2026.1 · Pre-revenue research prototype · Built by Herb Velez, Mythara Labs LLC

> SERE is defensive by recording. Anything offensive exists only inside the
> sandboxed simulation — it never strikes outward. This is a training
> concept, not a weapon and not a military capability.

Extracted from [herbievelezjr/Mythara_Archive](https://github.com/herbievelezjr/Mythara_Archive),
where the original copies remain as built.

## Doctrine (enforced in code)

- **Sandbox-only.** A specimen is never executed on the host. SERE analyzes an
  isolated copy only.
- **Detect:** the operator names an explicit specimen path. SERE invents
  nothing — no random threats, no fake source IPs.
- **Quarantine:** the original is moved to quarantine, verified gone from its
  source, with chain of custody kept.
- **Profile:** forensic profile of the contained copy — hashes, sizes,
  timestamps, permissions, type and embedded indicators. Indicators are never
  presented as attribution.
- **No hack-back, ever.** No firewall changes, no IP blocking, no remote
  retaliation. Egress sealed by design: SERE makes zero network calls.
- **No fabricated numbers.** Integrity is verified by hash comparison, not
  asserted. A failed step reports FAILED, never "100%".

Every action is appended to a tamper-evident hash-chained JSONL event log.

## Current capability — stated plainly

The implemented loop is **detect → quarantine → profile → log**. The
simulated adversary-evolution loop is not built. What exists is a disciplined,
auditable specimen-handling pipeline with a tamper-evident record — suitable
as the foundation for a training sandbox, not as an operational capability.

## Layout

- `sere_bot.py` — the core specimen-handling pipeline
- `sere_aries.py` — Aries integration
- `sere_course.py` — training course structure
- `sere_crucible.py` — crucible exercises
- `sere_slime.py` — slime-layer utilities
- `tests/` — focused test suite

Run the tests: `pytest tests/ -q`

## License

Source-available — see [LICENSE.md](LICENSE.md). Copyright © 2025 Herbert Velez Jr.
Mythara Labs LLC (Colorado domestic LLC, filed 2026-10-04; CO SOS ID #20268239831).
