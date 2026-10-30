# Fitbit

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

Fitbit is a wearable health and fitness platform — devices (trackers, smartwatches, smart scales) plus a
companion mobile app and cloud data services. Founded in 2007 and acquired by Google in January 2021,
Fitbit is now operated as part of Google's hardware portfolio alongside the Pixel Watch. The Fitbit Web API
exposes user activity, exercise, heart rate (including intraday and HRV), sleep with stage breakdowns, body
and weight, nutrition and water, devices, friends and leaderboards, and advanced sensor metrics — SpO2,
breathing rate, skin and core temperature, ECG, Irregular Rhythm Notifications, and Cardio Fitness Score
(VO2 Max). Authentication is OAuth 2.0 Authorization Code Grant with PKCE; default quota is 150 requests
per hour per authorized user per app. A webhook subscription system streams sync notifications for the
activities, body, foods, sleep, and userRevokedAccess collections. The Fitbit OS SDK lets developers ship
apps and clock faces directly to Versa, Sense, and other Fitbit devices using JavaScript/CSS/SVG. The
legacy Fitbit Web API is scheduled for deprecation in September 2026; new and migrated integrations should
target the successor Google Health API at developers.google.com/health, which uses Google OAuth 2.0 and
Google's modern infrastructure.

**Areas:** Wearables · Health · Fitness · Activity Tracking · Heart Rate · Sleep · Google · IoT · Wellness

## Fitbit on APIs.io

Everything profiled for Fitbit is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/fitbit/](https://apis.io/providers/fitbit/)** — or go straight to one of the APIs or properties below.

### APIs (3)

- [Fitbit User API](https://apis.io/apis/fitbit/fitbit-user-api/) — Read and update the authorized Fitbit user's profile including display name, gender, birthday, height, weight, locale, timezone, and unit preferences…
- [Fitbit Foods API](https://apis.io/apis/fitbit/fitbit-foods-api/) — The Foods API from Fitbit — 1 operation(s) for foods.
- [Fitbit Oauth2 API](https://apis.io/apis/fitbit/fitbit-oauth2-api/) — The Oauth2 API from Fitbit — 4 operation(s) for oauth2.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Fitbit Subscriptions Webhooks](https://apis.io/asyncapis/fitbit/fitbit-subscriptions-asyncapi/)

#### Event channels (2)

Individual events and webhooks the provider emits.

- [/subscriber](https://apis.io/channels/fitbit/subscriber/)
- [/subscriber/verify](https://apis.io/channels/fitbit/subscriber-verify/)

#### GraphQL (1)

GraphQL schemas.

- [Moved to /providers/fitbit/](https://apis.io/graphqls/fitbit/fitbit-graphql/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Fitbit Agentic Access](https://apis.io/agentic-access/fitbit/fitbit-agentic-access/)

#### JSON Schema (2)

The data models the API reads and writes.

- [Fitbit Activity Daily Summary](https://apis.io/schemas/fitbit/fitbit-activity-summary/)
- [Fitbit Sleep Log](https://apis.io/schemas/fitbit/fitbit-sleep-log/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Fitbit Context](https://apis.io/jsonld/fitbit/fitbit-context/)

#### Collections (17)

Postman and Open Collection request collections.

- [Fitbit Activity API](https://apis.io/collections/fitbit/open-fitbit-activity-api/)
- [Fitbit Authorization API](https://apis.io/collections/fitbit/open-fitbit-authorization-api/)
- [Fitbit Body API](https://apis.io/collections/fitbit/open-fitbit-body-api/)
- [Fitbit Devices API](https://apis.io/collections/fitbit/open-fitbit-devices-api/)
- [Fitbit ECG and Irregular Rhythm Notifications API](https://apis.io/collections/fitbit/open-fitbit-ecg-irn-api/)
- [Fitbit Activity Foods API](https://apis.io/collections/fitbit/open-fitbit-foods-api/)
- [Fitbit Friends API](https://apis.io/collections/fitbit/open-fitbit-friends-api/)
- [Fitbit Heart Rate API](https://apis.io/collections/fitbit/open-fitbit-heart-rate-api/)
- [Fitbit Nutrition API](https://apis.io/collections/fitbit/open-fitbit-nutrition-api/)
- [Fitbit Activity Foods Oauth2 API](https://apis.io/collections/fitbit/open-fitbit-oauth2-api/)
- [Fitbit Sleep API](https://apis.io/collections/fitbit/open-fitbit-sleep-api/)
- [Fitbit SpO2 / Breathing Rate / Temperature / HRV / VO2 Max API](https://apis.io/collections/fitbit/open-fitbit-spo2-breathing-temperature-api/)
- [Fitbit Subscriptions API](https://apis.io/collections/fitbit/open-fitbit-subscriptions-api/)
- [Fitbit Activity Foods User API](https://apis.io/collections/fitbit/open-fitbit-user-api/)
- [Fitbit Activity Foods API](https://apis.io/collections/fitbit/postman-fitbit-foods-api/)
- [Fitbit Activity Foods Oauth2 API](https://apis.io/collections/fitbit/postman-fitbit-oauth2-api/)
- [Fitbit Activity Foods User API](https://apis.io/collections/fitbit/postman-fitbit-user-api/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [Fitbit — asyncapi rules](https://apis.io/rules/fitbit/fitbit-asyncapi-spectral-rules/)
- [Fitbit — jsonschema rules](https://apis.io/rules/fitbit/fitbit-jsonschema-spectral-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Fitbit Authentication](https://apis.io/security/fitbit/fitbit-authentication/)
- [Fitbit Domain Security](https://apis.io/security/fitbit/fitbit-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Fitbit Scopes](https://apis.io/scopes/fitbit/fitbit-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Fitbit Plans Pricing](https://apis.io/plans/fitbit/fitbit-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Fitbit Rate Limits](https://apis.io/rate-limits/fitbit/fitbit-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Fitbit Finops](https://apis.io/finops/fitbit/fitbit-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://fitbit.com)
- [Documentation](https://dev.fitbit.com/build/reference/web-api/)
- [Getting started](https://dev.fitbit.com/getting-started/)
- [Pricing](https://store.google.com/category/watches_trackers)
- [Support](https://dev.fitbit.com/build/reference/web-api/troubleshooting-guide/)
- [Changelog](https://developers.google.com/health/release-notes)
- [Blog](https://community.fitbit.com/t5/Web-API-Development/Introducing-the-next-phase-of-the-Fitbit-Web-API/td-p/5821061)
- [Terms of service](https://www.fitbit.com/global/us/legal/terms-of-service)
- [Privacy policy](https://www.fitbit.com/global/us/legal/privacy-policy)
- [GitHub](https://github.com/Fitbit)

## API Evangelist rating

**Kin Score 54.3** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 62.5 |
| Contract quality | 67.2 |
| Contract governance | 13.6 |
| Operational transparency | 26.3 |
| Developer ergonomics | 58.3 |
| Access clarity | 60.5 |

**Agent readiness 30.4** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | negotiable (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | documented (partial credit) |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | documented (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 32.8** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/fitbit/](https://apis.io/providers/fitbit/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Fitbit: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/fitbit/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
