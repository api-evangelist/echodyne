# Echodyne

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
