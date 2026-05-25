# Fitbit (fitbit)
Fitbit is a wearable health and fitness platform — devices (trackers, smartwatches, smart scales) plus a companion mobile app and cloud data services. Founded in 2007 and acquired by Google in January 2021, Fitbit is now operated as part of Google's hardware portfolio alongside the Pixel Watch. The Fitbit Web API exposes user activity, exercise, heart rate (including intraday and HRV), sleep with stage breakdowns, body and weight, nutrition and water, devices, friends and leaderboards, and advanced sensor metrics — SpO2, breathing rate, skin and core temperature, ECG, Irregular Rhythm Notifications, and Cardio Fitness Score (VO2 Max). Authentication is OAuth 2.0 Authorization Code Grant with PKCE; the default quota is 150 requests per hour per authorized user per app. A webhook subscription system streams sync notifications for the activities, body, foods, sleep, and userRevokedAccess collections. The Fitbit OS SDK lets developers ship apps and clock faces directly to Versa, Sense, and other Fitbit devices using JavaScript/CSS/SVG.

> **Heads up — September 2026 deprecation.** The legacy Fitbit Web API is scheduled for turndown in September 2026. New and migrated integrations should target the successor [Google Health API](https://developers.google.com/health), which uses Google OAuth 2.0 and Google's modern infrastructure. See the [migration guide](https://developers.google.com/health/migration) and the [Fitbit Community announcement](https://community.fitbit.com/t5/Web-API-Development/Introducing-the-next-phase-of-the-Fitbit-Web-API/td-p/5821061).

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/fitbit/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - Wearable, Health, Fitness, Activity Tracking, Heart Rate, Sleep, Google, IoT

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## Authentication

OAuth 2.0 with four supported flows:

| Flow | Use Case |
|---|---|
| Authorization Code Grant with PKCE | Recommended for all new integrations (web, mobile, native, SPA) |
| Authorization Code Grant | Server-side web applications with a client secret |
| Implicit Grant | Browser-side / single-page apps (legacy) |
| Client Credentials | Fitbit Commerce APIs only — does **not** retrieve user data |

**Authorization endpoint:** `https://www.fitbit.com/oauth2/authorize`
**Token endpoint:** `https://api.fitbit.com/oauth2/token`
**Introspection:** `https://api.fitbit.com/1.1/oauth2/introspect`
**Revocation:** `https://api.fitbit.com/oauth2/revoke`

### Scopes

`activity`, `heartrate`, `location`, `nutrition`, `profile`, `settings`, `sleep`, `social`, `weight`, `oxygen_saturation`, `respiratory_rate`, `temperature`, `electrocardiogram`, `irregular_rhythm_notifications`, `cardio_fitness`.

### Application Types

| Type | Description |
|---|---|
| Personal | The developer's own Fitbit data. Intraday access is automatic. |
| Client | Mobile / single-page apps. Intraday access requires explicit approval. |
| Server | Multi-user backends that store tokens. Intraday access requires explicit approval. |

## Rate Limits

| Tier | Quota | Window |
|---|---|---|
| Authorized (per user, per app) | 150 requests | rolling 1 hour |
| Unauthorized / Client Credentials | 150 requests | rolling 1 hour per client IP / app |

Throttled responses return HTTP `429` with a `Retry-After` header (seconds).

See [`rate-limits/fitbit-rate-limits.yml`](rate-limits/fitbit-rate-limits.yml) for the API Commons Rate Limits 0.1 definition.

## APIs

### Fitbit Activity API
Read and write user activity, exercise logs, daily activity summaries (steps, distance, calories, floors, elevation), activity goals, the Fitbit exercise catalog, and Active Zone Minutes (AZM) time series. Day, period, and date-range queries.

**Human URL:** [https://dev.fitbit.com/build/reference/web-api/activity/](https://dev.fitbit.com/build/reference/web-api/activity/)

- [OpenAPI](openapi/fitbit-activity-api-openapi.yml)
- [JSON Schema — Activity Summary](json-schema/fitbit-activity-summary-schema.json)
- [JSON-LD](json-ld/fitbit-context.jsonld)
- [Naftiko Capability — Activity](capabilities/activity-activity.yaml)

### Fitbit Heart Rate API
Heart rate time series with resting heart rate, custom/default zones, and zone-minute breakdowns. Intraday detail at 1s / 1min / 5min / 15min resolution (with Intraday approval).

**Human URL:** [https://dev.fitbit.com/build/reference/web-api/heartrate-timeseries/](https://dev.fitbit.com/build/reference/web-api/heartrate-timeseries/)

- [OpenAPI](openapi/fitbit-heart-rate-api-openapi.yml)
- [Naftiko Capability — Heart Rate](capabilities/heart-rate-heart-rate.yaml)

### Fitbit Sleep API
Read, log, and delete sleep records with stage breakdowns (light, deep, REM, wake), sleep efficiency, time in bed, minutes asleep / awake / to fall asleep. Paginated list, date, and date-range queries, plus sleep goal management.

**Human URL:** [https://dev.fitbit.com/build/reference/web-api/sleep/](https://dev.fitbit.com/build/reference/web-api/sleep/)

- [OpenAPI](openapi/fitbit-sleep-api-openapi.yml)
- [JSON Schema — Sleep Log](json-schema/fitbit-sleep-log-schema.json)
- [Naftiko Capability — Sleep](capabilities/sleep-sleep.yaml)

### Fitbit Body API
Weight and body fat logs, BMI time series, weight and body fat goals. Aria smart scales and manual logs both flow into this surface.

**Human URL:** [https://dev.fitbit.com/build/reference/web-api/body/](https://dev.fitbit.com/build/reference/web-api/body/)

- [OpenAPI](openapi/fitbit-body-api-openapi.yml)
- [Naftiko Capability — Body](capabilities/body-body.yaml)

### Fitbit Nutrition API
Food, water, and meal logs; Fitbit foods database (search, get, create custom); meal goals, favorites, and frequent foods; daily macronutrient summaries.

**Human URL:** [https://dev.fitbit.com/build/reference/web-api/nutrition/](https://dev.fitbit.com/build/reference/web-api/nutrition/)

- [OpenAPI](openapi/fitbit-nutrition-api-openapi.yml)
- [Naftiko Capability — Nutrition](capabilities/nutrition-nutrition.yaml)

### Fitbit User API
Read and update the authorized user's profile — display name, gender, birthday, height, weight, locale, timezone, and unit preferences.

**Human URL:** [https://dev.fitbit.com/build/reference/web-api/user/](https://dev.fitbit.com/build/reference/web-api/user/)

- [OpenAPI](openapi/fitbit-user-api-openapi.yml)
- [Naftiko Capability — User Profile](capabilities/user-profile.yaml)

### Fitbit Devices API
List paired Fitbit devices, retrieve battery level and last sync time, identify the device model, and create/update/delete tracker alarms.

**Human URL:** [https://dev.fitbit.com/build/reference/web-api/devices/](https://dev.fitbit.com/build/reference/web-api/devices/)

- [OpenAPI](openapi/fitbit-devices-api-openapi.yml)
- [Naftiko Capability — Devices](capabilities/devices-devices.yaml)

### Fitbit Subscriptions API
Webhook subscriptions per user against the `activities`, `body`, `foods`, `sleep`, or `userRevokedAccess` collections. Fitbit POSTs to your registered Subscriber endpoint when data is available — eliminates polling.

**Human URL:** [https://dev.fitbit.com/build/reference/web-api/subscription/](https://dev.fitbit.com/build/reference/web-api/subscription/)

- [OpenAPI](openapi/fitbit-subscriptions-api-openapi.yml)
- [Naftiko Capability — Subscriptions](capabilities/subscriptions-subscriptions.yaml)

### Fitbit Friends API
Friends list and weekly friends leaderboard.

**Human URL:** [https://dev.fitbit.com/build/reference/web-api/friends/](https://dev.fitbit.com/build/reference/web-api/friends/)

- [OpenAPI](openapi/fitbit-friends-api-openapi.yml)

### Fitbit SpO2, Breathing Rate, Temperature, HRV, and Cardio Fitness API
Advanced sensor readings — SpO2 (blood oxygen), Breathing Rate, Skin and Core Temperature variation, Heart Rate Variability (RMSSD), and Cardio Fitness Score (VO2 Max). Per-day and per-date-range summaries; SpO2 / breathing rate / HRV support intraday detail with approval.

**Human URL:** [https://dev.fitbit.com/build/reference/web-api/spo2/](https://dev.fitbit.com/build/reference/web-api/spo2/)

- [OpenAPI](openapi/fitbit-spo2-breathing-temperature-api-openapi.yml)

### Fitbit ECG and Irregular Rhythm Notifications API
Electrocardiogram (ECG) readings on Sense / Sense 2 / Charge 5 / Charge 6 with waveform samples, sampling frequency, lead number, and the algorithm's result classification (Normal Sinus Rhythm / Atrial Fibrillation / Inconclusive). IRN alerts and enrollment profile.

**Human URL:** [https://dev.fitbit.com/build/reference/web-api/electrocardiogram/](https://dev.fitbit.com/build/reference/web-api/electrocardiogram/)

- [OpenAPI](openapi/fitbit-ecg-irn-api-openapi.yml)

### Fitbit Authorization API
OAuth 2.0 authorize / token / refresh / introspect / revoke endpoints.

**Human URL:** [https://dev.fitbit.com/build/reference/web-api/authorization/](https://dev.fitbit.com/build/reference/web-api/authorization/)

- [OpenAPI](openapi/fitbit-authorization-api-openapi.yml)

## Webhooks (Subscriptions)

Subscribe to a per-user collection — `activities`, `body`, `foods`, `sleep`, or `userRevokedAccess` — and Fitbit will POST a notification to your registered Subscriber URL whenever the user has new data in that collection. The subscriber endpoint must respond `204` on the verification challenge and on every notification.

## Fitbit OS SDK (On-Device Apps)

In addition to the cloud Web API, Fitbit publishes the **Fitbit OS SDK** for building apps and clock faces that run directly on Fitbit devices (Versa, Sense, Inspire, Charge). Apps are written in JavaScript / CSS / SVG and have access to on-device modules:

- **Sensors** — Accelerometer, Barometer, Gyroscope, Heart-rate, Body-presence
- **Motion & location** — Geolocation, Orientation
- **User context** — User-activity, User-profile, User-settings, Sleep, Exercise
- **Device** — Display, Haptics, Clock, Power
- **Communication** — Messaging (companion), File-transfer
- **Utilities** — Console, Crypto, FS, CBOR, JPEG, I18n, Permissions, System, Events

Tooling: [`fitbit-sdk-toolchain`](https://github.com/Fitbit/fitbit-sdk-toolchain), [`create-fitbit-app`](https://github.com/Fitbit/create-fitbit-app), [`developer-bridge`](https://github.com/Fitbit/developer-bridge).

Reference: [Device API Reference](https://dev.fitbit.com/build/reference/device-api/).

## Plans, Rate Limits, and FinOps

- [Plans (API Commons Plans 0.1)](plans/fitbit-plans-pricing.yml)
- [Rate Limits (API Commons Rate Limits 0.1)](rate-limits/fitbit-rate-limits.yml)
- [FinOps (FOCUS 1.3 aligned)](finops/fitbit-finops.yml)

## Common Properties

- [Fitbit Developer Portal](https://dev.fitbit.com/)
- [Web API Reference](https://dev.fitbit.com/build/reference/web-api/)
- [Device API Reference](https://dev.fitbit.com/build/reference/device-api/)
- [Getting Started](https://dev.fitbit.com/getting-started/)
- [Application Management](https://dev.fitbit.com/apps/)
- [Troubleshooting Guide](https://dev.fitbit.com/build/reference/web-api/troubleshooting-guide/)
- [Web API Development Forum](https://community.fitbit.com/t5/Web-API-Development/bd-p/dev)
- [Fitbit GitHub Organization](https://github.com/Fitbit)
- [Fitbit Premium](https://www.fitbit.com/global/us/products/premium)
- [Google Health API (successor)](https://developers.google.com/health)
- [Google Health API Migration Guide](https://developers.google.com/health/migration)

## Maintainers

- **Kin Lane** — [apievangelist.com](https://apievangelist.com) — [@apievangelist](https://twitter.com/apievangelist)
