# HSE dispatch map (verified 2026-09-15)

Artifact: `EmmmmDeee/Huntsman-Search-Engine-HSE-Termux-Android-Aarch64-Rust-` at `07cfe89`.
CI: workflow run 3154 on that SHA, conclusion success.

## Claim

HSE is a SpiderFoot-class module bus. Intelligence is dispatch policy, not a crawl frontier. A new dispatch crate is not required.

## Ownership

| Piece | Path |
|---|---|
| Pure convex policy | `src/core/convex/mod.rs` |
| Precomputed order | `src/core/dependency/mod.rs` (`dispatch_order_for`) |
| Run loop and skip gates | `src/core/engine/dispatch.rs` |
| Dead-module quarantine | `src/util/scraper_health.rs` + `src/core/engine/mod.rs` |
| Flags | `src/core/scan/options.rs` |
| Transport | `src/cli`, `src/api/scan_handlers/core.rs`, `src/web/js/state.js` |

## Tests that pin the claim

- `convex_order_fires_cheap_cascading_query_before_paid_terminal`
- `convex_order_has_same_membership_as_priority_order`
- engine tests that the loop uses `dispatch_order_for`
- `tests/halting.rs` skip-dead on automatic fan-out

## Not claimed

- Live `GET /api/v1/plan` prefix on the full 198-module registry (unobserved in the session that wrote this file).
- SpiderFoot CLI parity.
- Suitability of any seed kind.

## Why HSE `main` was not edited in that session

HSE requires Rust 1.98+. The session toolchain was 1.75. A mechanical split of `admission_rejection` out of `dispatch.rs` without a green `cargo test` on the project toolchain would violate RCVF Execute/Verify.
