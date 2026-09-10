# Aerem

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

## About Aerem

Aerem is a Mumbai-based "FinTech for CleanTech" group that finances, supplies and monitors rooftop
solar in India. The group comprises **Aerem Solutions Private Limited**, **NetZero Finance Private
Limited** (an RBI-licensed, solar-focused NBFC) and **Sunstore Solar Private Limited**. It
underwrites collateral-free rooftop solar loans for MSMEs and homeowners, provides supply chain
finance to solar EPC installers, runs the **SunStore** B2B solar equipment marketplace, operates
**AeROC** (an inverter-agnostic remote monitoring portal), ships the **Aerem App** and **Aerem
Partner App**, and certifies installers through **AAA — Aerem Asset Assurance**.

- Website: https://www.aerem.co/
- Products: https://sunstore.co/ · https://aeroc.aerem.co/ · https://partner.aerem.co/
- Group NBFC: https://netzerofin.com/

## API surface

**Aerem publishes no public API.** Contract discovery (enrichment STEP 0b) was run against every
host the record knows — `www.aerem.co`, `aerem.co`, `partner.aerem.co`, `aeroc.aerem.co`,
`auth.aerem.co`, `admin.aerem.co`, `sunstore.co` and `netzerofin.com` — probing for a REST OpenAPI
(`/openapi.json`, `/openapi.yaml`, `/swagger.json`, `/v1/openapi.json`, `/api-docs`, `/docs`,
`/redoc`, `/v3/api-docs`, `/api/*`), a GraphQL endpoint, an MCP `tools/list` manifest, an A2A agent
card at both `/.well-known/agent-card.json` and the legacy `/.well-known/agent.json`, and the full
`/.well-known/` document set. Every probe missed. There is no developer portal
(`/developers` → 404), no API section (`/api` → 404), no pricing page (`/pricing` → 404), no GitHub
organization, and no Postman workspace. Aerem's source control is a **private** Bitbucket workspace
(`AeremTech`).

Two real, provider-published artifacts were found and captured:

| Artifact | Method | Source |
|---|---|---|
| `llms/aeremc36d-llms.txt` | searched (verbatim) | https://www.aerem.co/llms.txt (HTTP 200) |
| `packages/aeremc36d-packages.yml` | searched | 5 first-party npm packages under the `@aerem` scope |

The `@aerem` npm packages are **internal engineering tooling** (an AI coding harness, a UI component
library, an analytics helper, a foundation engine) — not client libraries for an Aerem API — so this
profile deliberately emits `type: Packages` and **no** `SDKs` pointer.

Recorded absences, each with the HTTP status observed: `well-known/aeremc36d-well-known.yml`
(72 probes, 0 hits), `plans/aeremc36d-plans-pricing.yml` (`plan_count: 0`),
`rate-limits/aeremc36d-rate-limits.yml` (`limit_count: 0`). Domain security was probed into
`security/aeremc36d-domain-security.yml`.
