# Fitbit GraphQL Schema

Conceptual GraphQL schema for the Fitbit Web API — a wearable health and fitness platform acquired by Google in January 2021 and now part of Google's hardware portfolio alongside Pixel Watch. The legacy Fitbit Web API is scheduled for deprecation in September 2026; new integrations should target the [Google Health API](https://developers.google.com/health).

## Overview

The Fitbit Web API exposes REST endpoints organized into a dozen functional surfaces. This GraphQL schema unifies those surfaces into a single, typed query layer covering all major data domains.

**Base URL:** `https://api.fitbit.com/1`
**Auth:** OAuth 2.0 Authorization Code Grant with PKCE (recommended), Implicit Grant, or Client Credentials (commerce only)
**Rate Limit:** 150 requests per hour per authorized user per application; `429 Too Many Requests` with `Retry-After` header on overage

## Schema Source

`graphql/fitbit-schema.graphql`

## Covered API Surfaces

| Surface | Fitbit Web API Reference |
|---|---|
| User & Profile | `GET /user/-/profile` |
| Activity & Exercise | `GET /user/-/activities/date/{date}` |
| Heart Rate | `GET /user/-/activities/heart/date/{date}/1d` |
| Heart Rate Variability (HRV) | `GET /user/-/hrv/date/{date}` |
| Sleep | `GET /user/-/sleep/date/{date}` |
| SpO2 | `GET /user/-/spo2/date/{date}` |
| Breathing Rate | `GET /user/-/br/date/{date}` |
| Temperature | `GET /user/-/temp/skin/date/{date}` |
| Cardio Fitness Score | `GET /user/-/cardioscore/date/{date}` |
| Body (Weight / Fat / BMI) | `GET /user/-/body/log/weight/date/{date}` |
| Nutrition & Water | `GET /user/-/foods/log/date/{date}` |
| Devices & Alarms | `GET /user/-/devices` |
| Subscriptions (Webhooks) | `GET /user/-/apiSubscriptions` |
| ECG & IRN | `GET /user/-/ecg/list` |
| Friends & Leaderboard | `GET /user/-/friends/leaderboard` |
| Badges | `GET /user/-/badges` |
| Authorization | `POST /oauth2/token` |

## Named Types (56)

### Core User
- `User` — authorized Fitbit account with all top-level associations
- `UserProfile` — extended profile fields (height, weight, locale, unit preferences)
- `UserFeatures` — feature-flag set for the account

### Activity & Exercise
- `Activity` — daily activity summary (steps, distance, calories, floors, AZM)
- `ActiveZoneMinutes` — AZM breakdown by heart rate zone
- `ActivitySummary` — aggregated daily activity metrics
- `ActivityGoal` — user's activity targets
- `ActivityLog` — a logged activity or exercise session
- `ActivityLevelDetail` — granular activity level within a log
- `LogSource` — source of a log entry (device, app, or manual)
- `Distance` — distance breakdown by activity type
- `Exercise` — exercise type from the Fitbit catalog
- `ExerciseSet` — one set within a strength-training log
- `RunSummary` — run-specific exercise metrics
- `BikeSummary` — cycling-specific exercise metrics
- `SwimSummary` — swim-specific metrics (laps, lengths, stroke count)
- `GolfSummary` — golf-specific exercise metrics

### Time-Series Primitives
- `Steps` — steps time-series data point
- `DistanceSeries` — distance time-series data point
- `Calories` — calories time-series data point
- `ActiveMinutes` — active-minutes time-series data point

### Heart Rate
- `HeartRate` — daily heart rate record with resting HR and zones
- `HeartRateValue` — detail fields inside a daily heart rate record
- `HeartRateZone` — zone definition with caloriesOut and minutes
- `HeartRateTimeSeries` — time-series data point for heart rate
- `HeartRateIntraday` — intraday heart rate reading
- `HRV` — Heart Rate Variability container (summary + intraday minutes)
- `HRVSummary` — daily RMSSD and deep-sleep RMSSD
- `HRVMinute` — single intraday HRV reading
- `HRVValue` — RMSSD, coverage, HF, LF values

### Sleep
- `SleepLog` — full sleep record with stage data and efficiency
- `SleepStageData` — container for 30-second epoch data
- `SleepStage` — a single 30-second epoch (level + seconds)
- `SleepStageSummary` — aggregate minutes per stage (deep, light, REM, wake)
- `SleepStageStats` — count, minutes, and 30-day average for one stage
- `SleepSummary` — totals across main sleep and naps
- `SleepScore` — daily Sleep Score (Fitbit Premium metric)
- `SleepScoreValue` — overall score and quality description
- `SleepCompositionScore` — composition sub-score
- `SleepRevitalizationScore` — revitalization sub-score
- `SleepDurationScore` — duration sub-score
- `SleepGoal` — bedtime, wake time, and minimum duration target

### Advanced Sensors
- `SpO2` — blood oxygen saturation daily summary and intraday points
- `SpO2Minute` — intraday SpO2 reading
- `BreathingRate` — breathing rate by sleep stage
- `BreathingRateValue` — per-stage summaries
- `BreathingRateStageSummary` — average breathing rate for one stage
- `Temperature` — skin and core temperature with deviation
- `TemperatureValue` — nightly relative value and expected range
- `TemperatureRange` — min/max expected temperature
- `CardioFitnessScore` — VO2 Max record with confidence range
- `CardioFitnessValue` — VO2 Max string and numeric estimate

### Body Composition
- `WeightLog` — a weight log entry (weight, BMI, fat)
- `BodyFat` — a body fat percentage log entry
- `BodyComposition` — aggregate view (weight, BMI, fat)
- `BMI` — BMI time-series data point
- `Weight` — weight time-series data point
- `BodyGoal` — weight and body fat targets

### Nutrition & Water
- `Food` — food item from the Fitbit database or user-created
- `FoodLog` — a food log entry with nutritional values
- `LoggedFood` — food reference inside a log entry
- `FoodServing` — serving size definition
- `FoodUnit` — measurement unit (name and plural)
- `NutritionalValues` — full macro and micro nutrient breakdown (36 fields)
- `Meal` — saved meal collection
- `MealFood` — food item within a saved meal
- `NutritionSummary` — daily calorie budget vs intake
- `NutritionCaloriesSummary` — budget, food calories, net
- `NutritionGoals` — calorie targets
- `FoodPlan` — calorie deficit or surplus plan
- `FoodPlanSupply` — daily calorie supply target
- `WaterLog` — a water log entry
- `WaterGoal` — daily water intake target
- `WaterSummary` — daily intake and goal

### Devices & Alarms
- `Device` — paired Fitbit device (tracker, scale, watch)
- `DeviceModel` — model metadata
- `DeviceBattery` — battery level and last sync timestamp
- `Alarm` — tracker alarm with recurrence and snooze settings
- `AlarmTime` — wall-clock time with UTC offset

### Social & Gamification
- `Friend` — a Fitbit friend with leaderboard rank
- `FriendUser` — minimal user reference for friends
- `Leaderboard` — weekly friends leaderboard
- `LeaderboardEntry` — single leaderboard entry (rank, steps, AZM)
- `Badge` — a Fitbit achievement badge

### ECG & IRN
- `ECG` — ECG reading with waveform samples and result classification
- `IrregularRhythmNotification` — IRN alert record
- `IrregularRhythmNotificationEnrollment` — IRN feature enrollment status

### Subscriptions & Sync
- `Subscription` — a webhook subscription for event notifications
- `EventSubscription` — received subscription event notification
- `SubscriptionUpdate` — individual update within an event
- `SyncRecord` — device-to-cloud sync event record

### Authorization
- `OAuthToken` — OAuth 2.0 access token metadata
- `TokenIntrospection` — token introspection result

## Enums (9)

`UnitSystem`, `Gender`, `BatteryLevel`, `DeviceType`, `SleepType`, `ActivityLevel`, `HeartRateZoneName`, `EcgResultStatus`, `SubscriptionCollection`, `Period`, `IntradayDetailLevel`

## Scalars

`Date` (YYYY-MM-DD), `DateTime` (ISO 8601), `Time` (HH:mm), `JSON`

## Query Operations

The root `Query` type exposes 30 fields covering all API surfaces. Notable patterns:

- Most queries accept an optional `userId` (defaults to `-` for the authorized user)
- Time-series queries accept either a `period` enum or explicit `startDate`/`endDate`
- Intraday queries require a `detailLevel` and optional time window

## Mutation Operations

The root `Mutation` type exposes 32 fields for creating, updating, and deleting log entries, goals, alarms, subscriptions, meals, and custom foods, plus OAuth token management (refresh, revoke).

## Migration Note

The Fitbit Web API is in legacy maintenance mode following Google's acquisition. Fitbit developer accounts, OAuth apps, and API access were migrated to Google infrastructure in 2023. A full deprecation is scheduled for September 2026. New integrations should use the [Google Health API](https://developers.google.com/health) with standard Google OAuth 2.0.
