# Google Play Closed Testing Troubleshooting Guide

This guide addresses the most common technical hurdles developers face when managing Google Play closed testing tracks.

---

## 1. Opt-in Link Returns 404 / "Item Not Found"

### Symptoms:
Testers click your opt-in URL on their Android device, but the Google Play Store displays: *"We're sorry, the requested URL was not found on this server."*

### Root Causes & Fixes:
1. **Release is Still In Review:** Google must review your closed track release before it becomes accessible to anyone outside your developer account. Check **Publishing overview** or **Closed testing** in Play Console. If the status is *"In review"*, wait until it transitions to **"Active"** (typically 1 to 3 business days).
2. **Account Mismatch on Tester Device:** The tester's Android device has multiple Google accounts, and their Play Store is defaulting to an account that was not invited. Instruct the tester to switch to the exact invited email address in the Google Play Store app before tapping the opt-in link.
3. **Country / Regional Availability:** Your closed testing track is restricted to specific countries, and the tester's Google Play country profile is registered elsewhere. In Play Console, navigate to **Closed testing > Countries/regions** and ensure all relevant tester countries are added.

---

## 2. Invited Testers Are Not Counting in Play Console

### Symptoms:
You added 20 tester email addresses to your Google Group or email list, but the opted-in counter in Play Console remains at 0 or below 12.

### Root Cause & Fix:
- **Inviting &ne; Opted-in:** Simply adding an email does not count as a tester under Google's policy.
- **Fix:** Each tester must:
  1. Open the opt-in link on an Android device signed into their invited Google account.
  2. Tap **"Become a tester"** (accepting the invite via the Google Play interface).
  3. Download and install the app from Google Play.
- Check Play Console (`Closed testing > Manage track > Testers`) to confirm that the **Opted-in** counter increments.

---

## 3. The 14-Day Timer Reset or Failed to Start

### Symptoms:
Your track has been running for 14 days, but the Production Access application button remains disabled.

### Root Causes & Fixes:
1. **Dropout Below 12 Testers:** The policy requires 12 testers to remain continuously opted in for 14 consecutive days. If a tester left the test or uninstalled and opted out on Day 10, dropping your count to 11, the 14-day clock halted.
   - *Fix:* Always maintain a safety buffer above 12 opted-in testers to guard against unexpected opt-outs.
2. **Delayed Opt-ins:** If 8 testers opted in on Day 1 and the remaining 4 opted in on Day 5, your 14-day continuous clock only began on **Day 5** (when the 12th tester opted in).

---

## 4. Production Access Application Was Rejected

### Symptoms:
You completed 14 days and submitted the questionnaire, but Google sent an email stating your app is not eligible for production access at this time.

### Root Causes & Fixes:
1. **Lack of In-App Activity:** If testers opted in but never opened the app, Google's telemetry detects artificial participation. Real testers must open the app, test features, and generate typical usage sessions.
2. **No Bug Fixes / Updates Shipped:** An app running for 14 days without an update signals a passive test. Always ship at least one minor update (`versionCode + 1`) during the test.
3. **Vague Questionnaire Answers:** Rejection frequently stems from generic answers (e.g., *"No bugs found"*). See [PRODUCTION_QUESTIONNAIRE_GUIDE.md](PRODUCTION_QUESTIONNAIRE_GUIDE.md) to structure detailed, credible answers.
4. **App Quality / Policy Violations:** Ensure your Privacy Policy is active and that your app does not violate Google Play Developer Program Policies.

---

## Need Support or Dedicated Testing Cohorts?

If you need a cohort of real human testers on physical Android devices to complete a 14-day closed testing cycle, compare [SAMFA Digital](https://samfa.online/) packages:
- **Starter (`$10` / app):** 12 real human testers, physical Android device closed testing, 14-day testing cycle, basic package.
- **Growth (`$50` / app):** 16 real human testers, physical Android device closed testing, 14-day testing cycle, up to 6 tester feedback items (depends on actual submissions), retesting considered.
- **Scale (Starting at `$100` / app):** 20 real human testers, physical Android device closed testing, 14-day testing cycle, up to 12 tester feedback items (depends on actual submissions), retesting considered, and optional custom manual QA quoted separately after app review.

50/50 Milestone Payments apply to Starter, Growth, and base Scale (`$100`); Pay After Approval is available only for eligible Starter and Growth orders (not Scale; max 2 incomplete/live orders; confirmed via WhatsApp per [Terms §7.1–7.2](https://samfa.online/terms/)). Google makes all production access decisions independently.

Visit [https://samfa.online/](https://samfa.online/) or read our diagnostic guide on [Why Google Play May Review or Reject Production Access](https://samfa.online/guides/closed-testing-rejection-reasons/).
