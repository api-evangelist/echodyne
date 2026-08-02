# Echodyne

Echodyne Corp is a Kirkland, Washington radar platform company building metamaterials
electronically scanned array (MESA®) radar for defense, government, critical infrastructure,
uncrewed aircraft systems (UAS) and advanced air mobility (AAM). Products include the compact
K-band **EchoGuard**, the medium-range Ku-band **EchoShield**, the airborne **EchoFlight**, and
**EchoWare** — the software platform that manages a network of radars as a single instance and
exposes radar management and data output to external command-and-control systems.

- Website: https://www.echodyne.com/
- EchoWare: https://www.echodyne.com/radar-systems/echoware
- Customer Portal: https://portal.echodyne.com/s/login/
- Resource library: https://www.echodyne.com/library

## API posture

Echodyne markets "multiple data-rich output options available via API" and a headless mode in
which a C2 system drives the radar network directly. Radar data — range-Doppler spectrograms,
detections, measurements, tracks and radar status — moves in a proprietary format over TCP/IP
Gigabit (EchoGuard) and 10 Gbps / 1 Gbps Ethernet (EchoShield).

**No machine-readable contract is published on the open web.** Contract discovery on 2026-08-01
found no OpenAPI, Swagger, GraphQL, AsyncAPI, MCP server or A2A agent card on any Echodyne host;
`api.`, `docs.`, `developer.`, `support.`, `echoware.` and `status.` subdomains do not resolve.
API reference, manuals, tooling and the ATAK plugin are distributed through the login-gated
Customer Portal.

What Echodyne *does* serve anonymously:

- `https://www.echodyne.com/llms.txt` — a real, well-formed llms.txt
- `https://portal.echodyne.com/.well-known/openid-configuration` — OIDC discovery for the
  Salesforce Experience Cloud customer portal (the only public machine-readable API surface)

## Artifacts

| Dir | File | Method |
|---|---|---|
| `llms/` | `echodyne-llms.txt` | searched (verbatim) |
| `well-known/` | `echodyne-well-known.yml`, `echodyne-openid-configuration.json` | searched / probed |
| `authentication/` | `echodyne-authentication.yml` | searched |
| `scopes/` | `echodyne-scopes.yml` | searched |
| `security/` | `echodyne-domain-security.yml` | probed |
| `conformance/` | `echodyne-conformance.yml` | searched |
| `lifecycle/` | `echodyne-lifecycle.yml` | searched |
| `conventions/` | `echodyne-conventions.yml` | searched |
| `packages/` | `echodyne-packages.yml` | searched |
| `integrations/` | `_index.yml` | searched (listing-only) |
