# Google Play Closed Testing Master Checklist

Use this checklist alongside our [interactive web App Publishing Checklist](https://samfa.online/guides/google-play-app-publishing-checklist/) to track your app's progress through Google Play's 12-tester, 14-day closed testing requirement.

---

## Phase 1: Pre-Release & Build Readiness

- [ ] **Android App Bundle (`.aab`):** Built with release keystore signing and appropriate `versionCode`.
- [ ] **Target API Level:** Compliant with Google Play's current target SDK requirement.
- [ ] **Basic Stability:** Verified that the build does not crash on launch across multiple screen densities.
- [ ] **Network Resilience:** App handles intermittent Wi-Fi and mobile data transitions without freezing.
- [ ] **App Content & Store Presence:**
  - [ ] App Title (under 30 characters).
  - [ ] Short Description (under 80 characters).
  - [ ] Full Description (accurate feature breakdown).
  - [ ] High-resolution App Icon (512x512 PNG).
  - [ ] Feature Graphic (1024x500 PNG/JPEG).
  - [ ] At least 2 phone screenshots (16:9 or 9:16 portrait/landscape matching Play Console specifications).
- [ ] **Mandatory Policies:**
  - [ ] Valid, publicly accessible Privacy Policy URL added in Play Console (`HTTP 200 OK`, no login wall).
  - [ ] Content Rating (IARC) questionnaire completed.
  - [ ] Target Audience and Content declarations completed.
  - [ ] Data Safety form accurately filled out reflecting all collected data and third-party SDKs.
  - [ ] App Access reviewer instructions/demo credentials provided if any flow requires login, OTP, or paywall access.

---

## Phase 2: Closed Testing Track Setup

- [ ] In Google Play Console, navigate to **Testing > Closed testing** (never **Internal testing** for the 12-tester requirement).
- [ ] Use **Closed testing - Alpha** or create a dedicated closed testing track.
- [ ] Under **Countries / regions**, enable target tester countries (or **All countries / regions** for distributed cohorts).
- [ ] Select tester management method under the **Testers** tab:
  - [ ] **Google Groups (Recommended):** Create a group at `groups.google.com`, add your testers, and link the group email.
  - [ ] **Email List:** Upload a `.csv` or enter tester Gmail addresses, **tick the checkbox next to the list**, and click **Save changes**.
- [ ] Create a new release, upload the signed `.aab`, and enter clear Release Notes explaining key workflows to test.
- [ ] Submit pending edits through **Publishing overview** (if managed publishing is active) and wait for initial review.
- [ ] Verify that release status changes from *In review* to **Available to testers** before distributing the opt-in link.
- [ ] Copy the official **Join on Android** or **Join on the Web** opt-in URL from the Testers tab.

---

## Phase 3: Tester Onboarding & Active Tracking

- [ ] Recruit at least 12 distinct real testers on physical Android devices (choosing 16 or 20 real testers maintains a safety buffer against unexpected uninstalls).
- [ ] Distribute the opt-in URL to testers with clear instructions:
  1. Open the link on a physical Android device while signed into the exact invited Google account.
  2. Tap **"Become a tester"** (accepting the invite via Google Play).
  3. Install the application directly from the Google Play Store listing (sideloaded APKs never count).
- [ ] Navigate to **Closed testing > Manage track > Testers** in Play Console and confirm **Opted-in Testers &ge; 12**.
- [ ] Record Day 1 start date in [TESTER_TRACKING_TEMPLATE.csv](TESTER_TRACKING_TEMPLATE.csv).
- [ ] Check daily opt-in counts and Android Vitals crash/ANR metrics throughout all 14 continuous days.
- [ ] Push at least one meaningful update (`versionCode + 1`) during the 14-day cycle addressing surfaced issues (pushing updates does not reset your 14-day clock while the track remains live and 12+ testers stay opted in).
- [ ] Log actionable tester feedback, crash fixes, and UI adjustments in writing ([Tester Feedback & Testing Quality Guide](https://samfa.online/guides/google-play-tester-feedback-and-testing-quality/)).

---

## Phase 4: Production Access Application

- [ ] Confirmed that **14 continuous days** have elapsed with **&ge; 12 opted-in testers** and keep the closed track + testers active while review runs.
- [ ] Under Dashboard / Release overview, click **Apply for Production Access**.
- [ ] Complete all 3 sections (~8 questions) of the production access questionnaire using accurate, app-specific examples:
  - See [PRODUCTION_QUESTIONNAIRE_GUIDE.md](PRODUCTION_QUESTIONNAIRE_GUIDE.md) and our [full Questionnaire Answers Framework](https://samfa.online/guides/google-play-production-access-questionnaire-answers/).
- [ ] Confirm that your production store listing, Data Safety declarations, App Access demo logins, and country availability are accurate.
- [ ] Submit application and monitor Google Play Console for review decision.

---

*Checklist provided by [SAMFA Digital](https://samfa.online) &mdash; Google Play Closed Testing Services & Android QA. See the interactive browser version at [samfa.online/guides/google-play-app-publishing-checklist/](https://samfa.online/guides/google-play-app-publishing-checklist/).*
