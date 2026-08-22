# Fitbit (fitbit)

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

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/fitbit/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/fitbit/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Wearable
- Health
- Fitness
- Activity Tracking
- Heart Rate
- Sleep
- Google
- IoT

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-30

## APIs

### Fitbit Activity API

Read and write user activity, exercise logs, daily activity summaries (steps, distance, calories, floors, elevation), activity goals, the Fitbit exercise catalog, and Active Zone Minutes (AZM) time series. Supports per-day, per-period, and per-date-range queries.

- **Human URL:** [https://dev.fitbit.com/build/reference/web-api/activity/](https://dev.fitbit.com/build/reference/web-api/activity/)

#### Tags

- Activity
- Fitness
- Steps
- Active Zone Minutes
- Wearable

#### Properties

- [Documentation](https://dev.fitbit.com/build/reference/web-api/activity/)
- [Documentation](https://dev.fitbit.com/build/reference/web-api/active-zone-minutes-timeseries/)
- [OpenAPI](openapi/fitbit-activity-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fitbit-activity-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fitbit-activity-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/fitbit-activity-summary-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/fitbit-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### Fitbit Heart Rate API

Retrieve heart rate time series including resting heart rate, custom and default heart rate zones, and zone-minute breakdowns. Intraday endpoints expose 1-second, 1-minute, 5-minute, or 15-minute detail-level series and require explicit Intraday access approval.

- **Human URL:** [https://dev.fitbit.com/build/reference/web-api/heartrate-timeseries/](https://dev.fitbit.com/build/reference/web-api/heartrate-timeseries/)

#### Tags

- Heart Rate
- Cardiovascular
- Wearable

#### Properties

- [Documentation](https://dev.fitbit.com/build/reference/web-api/heartrate-timeseries/)
- [Documentation](https://dev.fitbit.com/build/reference/web-api/intraday/)
- [OpenAPI](openapi/fitbit-heart-rate-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fitbit-heart-rate-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fitbit-heart-rate-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fitbit Sleep API

Read, log, and delete sleep records with stage breakdowns (light, deep, REM, wake), sleep efficiency, time in bed, minutes asleep, minutes awake, and minutes to fall asleep. Supports paginated list queries, date queries, date-range queries, and sleep goal management.

- **Human URL:** [https://dev.fitbit.com/build/reference/web-api/sleep/](https://dev.fitbit.com/build/reference/web-api/sleep/)

#### Tags

- Sleep
- Sleep Stages
- Wearable

#### Properties

- [Documentation](https://dev.fitbit.com/build/reference/web-api/sleep/)
- [OpenAPI](openapi/fitbit-sleep-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fitbit-sleep-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fitbit-sleep-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/fitbit-sleep-log-schema.json) — [JSON Schema](https://json-schema.org/specification)

### Fitbit Body API

Read and write weight and body fat log entries, BMI time series, and body weight / body fat goals. Aria scales and manual logs both flow into this surface.

- **Human URL:** [https://dev.fitbit.com/build/reference/web-api/body/](https://dev.fitbit.com/build/reference/web-api/body/)

#### Tags

- Body
- Weight
- BMI
- Body Fat

#### Properties

- [Documentation](https://dev.fitbit.com/build/reference/web-api/body/)
- [OpenAPI](openapi/fitbit-body-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fitbit-body-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fitbit-body-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fitbit Nutrition API

Read and write food, water, and meal logs; access the Fitbit foods database (search, get by ID, create custom foods); manage meal goals, favorites, and frequent foods; and read daily macronutrient summaries (calories, carbs, fat, fiber, protein, sodium, water).

- **Human URL:** [https://dev.fitbit.com/build/reference/web-api/nutrition/](https://dev.fitbit.com/build/reference/web-api/nutrition/)

#### Tags

- Nutrition
- Food
- Water
- Calories

#### Properties

- [Documentation](https://dev.fitbit.com/build/reference/web-api/nutrition/)
- [OpenAPI](openapi/fitbit-nutrition-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fitbit-nutrition-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fitbit-nutrition-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fitbit User API

Read and update the authorized Fitbit user's profile including display name, gender, birthday, height, weight, locale, timezone, and unit preferences (distance, weight, water, glucose, temperature).

- **Human URL:** [https://dev.fitbit.com/build/reference/web-api/user/](https://dev.fitbit.com/build/reference/web-api/user/)

#### Tags

- User
- Profile
- Settings

#### Properties

- [Documentation](https://dev.fitbit.com/build/reference/web-api/user/)
- [OpenAPI](openapi/fitbit-user-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fitbit-user-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fitbit-user-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fitbit Devices API

List paired Fitbit devices, retrieve battery level and last sync timestamps, identify the device model (deviceVersion), and create, update, and delete tracker alarms.

- **Human URL:** [https://dev.fitbit.com/build/reference/web-api/devices/](https://dev.fitbit.com/build/reference/web-api/devices/)

#### Tags

- Devices
- Wearable
- Alarms

#### Properties

- [Documentation](https://dev.fitbit.com/build/reference/web-api/devices/)
- [OpenAPI](openapi/fitbit-devices-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fitbit-devices-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fitbit-devices-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fitbit Subscriptions API

Webhook-based notification system. Subscribe per user to the activities, body, foods, sleep, or userRevokedAccess collections; Fitbit POSTs to your registered Subscriber endpoint when new data is available, eliminating polling.

- **Human URL:** [https://dev.fitbit.com/build/reference/web-api/subscription/](https://dev.fitbit.com/build/reference/web-api/subscription/)

#### Tags

- Webhooks
- Subscriptions
- Notifications

#### Properties

- [Documentation](https://dev.fitbit.com/build/reference/web-api/subscription/)
- [OpenAPI](openapi/fitbit-subscriptions-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fitbit-subscriptions-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fitbit-subscriptions-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](asyncapi/fitbit-subscriptions-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)

### Fitbit Friends API

Read the authorized user's Fitbit friends list and weekly friends leaderboard rankings.

- **Human URL:** [https://dev.fitbit.com/build/reference/web-api/friends/](https://dev.fitbit.com/build/reference/web-api/friends/)

#### Tags

- Social
- Friends
- Leaderboard

#### Properties

- [Documentation](https://dev.fitbit.com/build/reference/web-api/friends/)
- [OpenAPI](openapi/fitbit-friends-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fitbit-friends-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fitbit-friends-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fitbit SpO2, Breathing Rate, Temperature, HRV, and Cardio Fitness API

Advanced sensor readings from supported Fitbit devices — SpO2 (blood oxygen saturation), Breathing Rate, Skin Temperature and Core Temperature variation, Heart Rate Variability (RMSSD), and Cardio Fitness Score (VO2 Max). Each metric supports per-day and per-date-range summary queries; SpO2, breathing rate, and HRV additionally support intraday detail with Intraday access approval.

- **Human URL:** [https://dev.fitbit.com/build/reference/web-api/spo2/](https://dev.fitbit.com/build/reference/web-api/spo2/)

#### Tags

- SpO2
- Breathing Rate
- Temperature
- HRV
- VO2 Max
- Cardio Fitness

#### Properties

- [Documentation](https://dev.fitbit.com/build/reference/web-api/spo2/)
- [Documentation](https://dev.fitbit.com/build/reference/web-api/breathing-rate/)
- [Documentation](https://dev.fitbit.com/build/reference/web-api/temperature/)
- [Documentation](https://dev.fitbit.com/build/reference/web-api/heartrate-variability/)
- [Documentation](https://dev.fitbit.com/build/reference/web-api/cardio-fitness-score/)
- [OpenAPI](openapi/fitbit-spo2-breathing-temperature-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fitbit-spo2-breathing-temperature-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fitbit-spo2-breathing-temperature-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fitbit ECG and Irregular Rhythm Notifications API

Access Electrocardiogram (ECG) readings recorded on Fitbit Sense, Sense 2, and Charge 5/6 devices, and access Irregular Rhythm Notifications (IRN) including alerts and feature enrollment. ECG readings include waveform samples, sampling frequency, lead number, and the algorithm's result classification (Normal Sinus Rhythm, Atrial Fibrillation, Inconclusive).

- **Human URL:** [https://dev.fitbit.com/build/reference/web-api/electrocardiogram/](https://dev.fitbit.com/build/reference/web-api/electrocardiogram/)

#### Tags

- ECG
- Electrocardiogram
- Irregular Rhythm Notifications
- Atrial Fibrillation
- Cardiac Health

#### Properties

- [Documentation](https://dev.fitbit.com/build/reference/web-api/electrocardiogram/)
- [Documentation](https://dev.fitbit.com/build/reference/web-api/irregular-rhythm-notifications/)
- [OpenAPI](openapi/fitbit-ecg-irn-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fitbit-ecg-irn-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fitbit-ecg-irn-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Fitbit Authorization API

OAuth 2.0 authorization endpoints. Supports Authorization Code Grant with PKCE (recommended), Authorization Code Grant, Implicit Grant, and Client Credentials (for Fitbit Commerce APIs that do not retrieve user data). Tokens can be introspected, refreshed, or revoked.

- **Human URL:** [https://dev.fitbit.com/build/reference/web-api/authorization/](https://dev.fitbit.com/build/reference/web-api/authorization/)

#### Tags

- OAuth
- Authentication
- Authorization
- Security

#### Properties

- [Documentation](https://dev.fitbit.com/build/reference/web-api/authorization/)
- [OpenAPI](openapi/fitbit-authorization-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/fitbit-authorization-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/fitbit-authorization-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://www.fitbit.com)
- [Portal](https://dev.fitbit.com/)
- [Documentation](https://dev.fitbit.com/build/reference/web-api/)
- [Documentation](https://dev.fitbit.com/build/reference/device-api/)
- [Getting Started](https://dev.fitbit.com/getting-started/)
- [Documentation](https://dev.fitbit.com/build/reference/web-api/authorization/)
- [Support](https://dev.fitbit.com/build/reference/web-api/troubleshooting-guide/)
- [Errors](https://dev.fitbit.com/build/reference/web-api/troubleshooting-guide/error-handling/)
- [Errors](https://dev.fitbit.com/build/reference/web-api/troubleshooting-guide/error-messages/)
- [Rate Limits](https://dev.fitbit.com/build/reference/web-api/rate-limits/)
- [Documentation](https://dev.fitbit.com/build/reference/web-api/intraday/)
- [Documentation](https://dev.fitbit.com/build/reference/web-api/subscription/)
- [Sign Up](https://dev.fitbit.com/apps/)
- [GitHub Organization](https://github.com/Fitbit)
- [SDK](https://github.com/Fitbit/fitbit-sdk-toolchain)
- [SDK](https://github.com/Fitbit/create-fitbit-app)
- [Tool](https://github.com/Fitbit/developer-bridge)
- [Code Examples](https://github.com/Fitbit/sdk-oauth)
- [Code Examples](https://github.com/Fitbit/sdk-hr-meter)
- [Code Examples](https://github.com/Fitbit/ossapps)
- [Tool](https://github.com/Fitbit/golden-gate)
- [Tool](https://github.com/Fitbit/bitgatt)
- [Plans](https://www.fitbit.com/global/us/products/premium)
- [Pricing](https://store.google.com/category/watches_trackers)
- [LinkedIn](https://www.linkedin.com/company/fitbit)
- [Twitter](https://twitter.com/fitbit)
- [YouTube](https://www.youtube.com/user/fitbit)
- [Support](https://help.fitbit.com/)
- [Forum](https://community.fitbit.com/)
- [Forum](https://community.fitbit.com/t5/Web-API-Development/bd-p/dev)
- [Terms of Service](https://www.fitbit.com/global/us/legal/terms-of-service)
- [Privacy Policy](https://www.fitbit.com/global/us/legal/privacy-policy)
- [Terms of Service](https://dev.fitbit.com/legal/platform-terms-of-service/)
- [Documentation](https://developers.google.com/health)
- [Documentation](https://developers.google.com/health/migration)
- [Changelog](https://developers.google.com/health/release-notes)
- [Blog](https://community.fitbit.com/t5/Web-API-Development/Introducing-the-next-phase-of-the-Fitbit-Web-API/td-p/5821061)
- [Portal](https://about.google/intl/en/products/devices-services/fitbit/)
- [Blog](https://blog.google/products/fitbit/)
- [Plans](plans/fitbit-plans-pricing.yml)
- [Rate Limits](rate-limits/fitbit-rate-limits.yml)
- [Fin Ops](finops/fitbit-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
