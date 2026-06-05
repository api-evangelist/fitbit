# Fitbit (fitbit)

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
