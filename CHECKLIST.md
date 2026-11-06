# Google Play Closed Testing Master Checklist

Use this checklist to track your app's progress through Google Play's 12-tester, 14-day closed testing requirement.

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
  - [ ] At least 2 phone screenshots (minimum 1080p, 16:9 or 18:9 aspect ratio).
- [ ] **Mandatory Policies:**
  - [ ] Valid, publicly accessible Privacy Policy URL added in Play Console.
  - [ ] Content Rating (IARC) questionnaire completed.
  - [ ] Target Audience and Content declarations completed.
  - [ ] Data Safety form accurately filled out reflecting all collected data and third-party SDKs.

---

## Phase 2: Closed Testing Track Setup

- [ ] In Google Play Console, navigate to **Testing > Closed testing**.
- [ ] Create a closed testing track (e.g., "Alpha" or "Closed Alpha").
- [ ] Select tester management method:
  - [ ] **Google Groups (Recommended):** Create a group at `groups.google.com`, add your testers, and link the group email.
  - [ ] **Email List:** Upload a `.csv` or enter tester Gmail addresses directly.
- [ ] Create a new release, upload the `.aab`, and enter clear Release Notes.
- [ ] Submit the release for Google's pre-release review.
- [ ] Verify that release status displays **Active** before distributing the opt-in link.
- [ ] Copy the official **Join on Android** or **Join on the Web** opt-in URL from the Testers tab.

---

## Phase 3: Tester Onboarding & Active Tracking

- [ ] Recruit at least 15–20 testers (maintaining a buffer above the 12-tester minimum).
- [ ] Distribute the opt-in URL to testers with clear instructions:
  1. Open the link on a physical Android device while signed into the invited Google account.
  2. Tap **"Become a tester"** (accepting the invite via Google Play).
  3. Install the application from the Google Play Store prompt.
- [ ] Navigate to **Closed testing > Manage track > Testers** in Play Console and confirm:
  - [ ] **Opted-in Testers &ge; 12**.
- [ ] Record Day 1 start date in [TESTER_TRACKING_TEMPLATE.csv](TESTER_TRACKING_TEMPLATE.csv).
- [ ] Check daily headcount to ensure the opted-in number never drops below 12.
- [ ] Push at least one minor update (`versionCode + 1`) during the 14-day cycle to demonstrate active development.
- [ ] Log all bug reports, UI suggestions, and crash details in writing.

---

## Phase 4: Production Access Application

- [ ] Confirmed that **14 continuous days** have elapsed with **&ge; 12 opted-in testers**.
- [ ] Under Release overview, click **Apply for Production Access**.
- [ ] Complete the production access questionnaire using specific, documented feedback examples:
  - See [PRODUCTION_QUESTIONNAIRE_GUIDE.md](PRODUCTION_QUESTIONNAIRE_GUIDE.md) for recommended frameworks.
- [ ] Confirm that your production store listing, pricing, and country availability are finalized.
- [ ] Submit application and monitor Google Play Console for review decision.

---

*Checklist provided by [SAMFA Digital](https://samfa.online) &mdash; Google Play Closed Testing Services & Android QA.*
