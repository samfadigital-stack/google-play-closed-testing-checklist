# Google Play Closed Testing Checklist: 12 Testers for 14 Days

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Platform: Android](https://img.shields.io/badge/Platform-Android-green.svg)](https://developer.android.com/)
[![Google Play Console](https://img.shields.io/badge/Google%20Play-Console%20Ready-brightgreen.svg)](https://play.google.com/console/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

An open-source, battle-tested operational checklist for Android developers, indie creators, and engineering teams navigating Google Play's mandatory closed-testing requirement (**12 testers continuously opted in for at least 14 consecutive days**) before applying for production release access.

Maintained with real-world testing telemetry by [SAMFA Digital](https://samfa.online) — dedicated to helping app developers launch reliably on Google Play.

---

## Table of Contents

1. [Understanding the Requirement](#understanding-the-requirement)
2. [Phase 1: Pre-Testing Readiness & Technical Audit](#phase-1-pre-testing-readiness--technical-audit)
3. [Phase 2: Closed Testing Track Setup (Google Play Console)](#phase-2-closed-testing-track-setup-google-play-console)
4. [Phase 3: Tester Onboarding & Verification Protocol](#phase-3-tester-onboarding--verification-protocol)
5. [Phase 4: 14-Day Active Testing Protocol](#phase-4-14-day-active-testing-protocol)
6. [Phase 5: Production Access Questionnaire Preparation](#phase-5-production-access-questionnaire-preparation)
7. [Common Rejection Triggers & How to Prevent Them](#common-rejection-triggers--how-to-prevent-them)
8. [Comprehensive Educational Resources](#comprehensive-educational-resources)
9. [Contributing](#contributing)
10. [License](#license)

---

## Understanding the Requirement

Since November 13, 2023, Google mandates that all developers with personal Play Console accounts created after that date must run a closed test for their app with **a minimum of 12 testers opted in continuously for at least 14 consecutive days** before they can request access to publish their app to Production.

### The Golden Rules

- **12 Unique Testers**: Exactly 12 or more independent Google accounts must accept the closed-testing invitation.
- **Continuous 14 Days**: If an opted-in tester uninstalls or opts out and your total active count drops below 12, Google's internal 14-day counter resets or pauses. *Recommendation: Recruit 16 to 20 testers as an active buffer.*
- **Genuine Device Engagement**: Automated bots or inactive installations are heavily flagged by Google Play Console automated review algorithms. Testers must install the app, grant requested permissions, and interact across multiple sessions.
- **Evidence of Feedback Loop**: The developer must prove that testers engaged with the app and provided qualitative bug reports or usability feedback during the testing period.

---

## Phase 1: Pre-Testing Readiness & Technical Audit

Before uploading an Android App Bundle (AAB) to your closed testing track, verify that the application satisfies baseline Android engineering standards.

- [ ] **Android App Bundle (.aab)** generated with Release build variant and ProGuard/R8 obfuscation enabled.
- [ ] **Target API Level**: Set to target the latest Android API level required by Google Play (API Level 34+ / 35).
- [ ] **App Signing**: Google Play App Signing enabled with secure release keystore.
- [ ] **Crash & ANR Monitoring**: Firebase Crashlytics, Bugsnag, or Sentry integrated and verified to capture exceptions.
- [ ] **In-App Feedback Mechanism**: A dedicated in-app feedback modal, email intent, or Discord/WhatsApp/Slack link so testers can report issues without rating publicly.
- [ ] **Privacy Policy URL**: Live, publicly accessible privacy policy page detailing all permissions, third-party SDKs, and data retention policies (e.g., hosted on your verified domain).
- [ ] **Data Safety Form**: Accurately completed in Play Console matching your actual app dependencies (location, identifiers, financial data, analytics).
- [ ] **Test Credentials**: Working demo login credentials configured in Play Console App Content under **App access** if your app requires authentication.

---

## Phase 2: Closed Testing Track Setup (Google Play Console)

Configure your closed testing track according to Google's strict workflow.

- [ ] **Create Closed Testing Track**:
  - Navigate to **Release > Testing > Closed testing**.
  - Click **Create track** (e.g., name it `Alpha` or `Closed Beta`).
- [ ] **Configure Countries / Regions**:
  - Select all target countries where your testers reside.
  - *Tip: If recruiting global testers, select all countries to prevent geographical installation blocks.*
- [ ] **Tester List Management**:
  - Select **Email lists** or **Google Groups**.
  - Enter all tester Google account email addresses.
  - Recommended minimum: **16 to 20 testers** to ensure you remain safely above the 12-tester threshold.
- [ ] **Create New Release**:
  - Upload your signed `.aab` file.
  - Fill in descriptive release notes outlining features to test.
  - Click **Review release** and **Start rollout to Closed testing**.
- [ ] **Wait for Google Review**:
  - Closed testing tracks must pass initial automated and policy review (typically 1 to 3 days).
  - Do **not** send opt-in links to testers until the release status changes to **Available to testers**.

---

## Phase 3: Tester Onboarding & Verification Protocol

Having a list of emails is not enough; testers must explicitly opt in.

- [ ] **Retrieve Opt-In Links**:
  - In Play Console under your closed track, scroll to **How testers join your test**.
  - Copy both the **Web link** (`https://play.google.com/apps/testing/com.your.packagename`) and the **Android link**.
- [ ] **Deliver Structured Onboarding Instructions**:
  - Provide testers with step-by-step instructions:
    1. Click the Web Opt-in link while signed into their invited Google account.
    2. Click **"Become a tester"**.
    3. Click **"Download it on Google Play"** to install the build on a physical Android device.
- [ ] **Verify Opt-In Status in Play Console**:
  - Navigate to your closed testing track overview.
  - Confirm that the **Opted-in testers** counter displays at least **12** (target 16+).
- [ ] **Device & OS Diversity Check**:
  - Ensure testers represent diverse Android OS versions (Android 11, 12, 13, 14, 15) and OEM form factors (Samsung, Xiaomi, Pixel, Motorola) to reveal real compatibility edge cases.

---

## Phase 4: 14-Day Active Testing Protocol

Maintain continuous engagement throughout the 14 consecutive calendar days.

- [ ] **Day 1: Baseline Smoke Testing**:
  - Confirm all testers have installed the app and completed the primary onboarding/registration flow.
  - Monitor Crashlytics for startup crashes or API failures.
- [ ] **Days 2–4: Core Feature Exercise**:
  - Direct testers to stress core features (database queries, push notifications, offline mode, background services).
  - Collect early UX feedback on navigation clarity and layout responsiveness.
- [ ] **Days 5–8: Push an Incremental Update (AAB v1.0.1)**:
  - Address bug reports collected during Days 1–4.
  - Upload a new release build to the closed track.
  - *Why this matters*: When reviewing your production access request, Google explicitly checks whether developer activity and updates took place during closed testing.
- [ ] **Days 9–11: Performance & Edge Case Testing**:
  - Test low-memory situations, network drops (airplane mode toggles), and permission revocations.
  - Verify ANR (Application Not Responding) rates remain at 0.00% in Play Console Vitals.
- [ ] **Days 12–14: Final Stability & Readiness Sign-off**:
  - Ensure opted-in count has remained at or above 12 every single day.
  - Compile feedback notes, bug resolution logs, and tester testimonials.
  - Confirm the Play Console dashboard displays the prompt: **"Apply for production"**.

---

## Phase 5: Production Access Questionnaire Preparation

When the 14-day threshold is reached, Google Play Console unlocks the **"Apply for production"** application. Prepare compelling, substantive answers.

- [ ] **Question: How did you recruit your testers?**:
  - Provide specific, legitimate details (e.g., professional QA community, colleagues, beta testing user cohort).
  - Avoid generic one-liners like *"friends and family"* or *"online testing service"*.
- [ ] **Question: What feedback did you receive from testers?**:
  - Detail 2 to 3 concrete issues uncovered during testing (e.g., UI clipping on smaller screens, edge-case null pointer on token refresh).
- [ ] **Question: What changes did you make based on this feedback?**:
  - Reference specific commit fixes, UX enhancements, and the incremental build version pushed to closed testing.
- [ ] **Question: Why do you believe your app is ready for production?**:
  - Summarize your stability metrics: zero crash sessions, tested across diverse hardware, high user task completion rate.

---

## Common Rejection Triggers & How to Prevent Them

| Pitfall | Root Cause | Preventive Measure |
| :--- | :--- | :--- |
| **Silent Rejection / Extended Testing** | Google flags low engagement or automated bot installs. | Ensure human testers open the app regularly and engage in multi-screen interactions. |
| **Counter Reset to Day 0** | Opted-in tester count dropped to 11 due to accidental opt-out. | Maintain a safety buffer of 16 to 20 active testers. |
| **Vague Questionnaire Responses** | Boilerplate, copy-paste answers in the production questionnaire. | Provide granular technical details, actual bugs fixed, and release iterations. |
| **Zero App Updates during Testing** | Developer uploaded v1.0.0 and never released an update. | Release at least one update (v1.0.1) addressing reported tester feedback. |
| **Target SDK Non-Compliance** | Outdated Gradle targetSdkVersion. | Ensure project targets Android 14 (API 34) or 15 (API 35). |

---

## Comprehensive Educational Resources

For step-by-step operational tutorials, visual walkthroughs, and Play Console compliance guides, review our comprehensive knowledge base:

- **Complete Step-by-Step Guide**: [Google Play 12 Testers for 14 Days Closed Testing: The Complete Developer Guide](https://samfa.online/guides/google-play-12-testers-14-days/)
- **Production Access Application**: [How to Apply for Google Play Production Access and Pass Review](https://samfa.online/guides/google-play-production-access/)
- **Rejection Analysis & Solutions**: [Common Google Play Closed Testing Rejection Reasons and How to Fix Them](https://samfa.online/guides/closed-testing-rejection-reasons/)
- **Official Documentation**: [Google Play Console Help — Set up an open, closed, or internal test](https://support.google.com/googleplay/android-developer/answer/9845334)

---

## Contributing

Contributions, issues, and feature requests are welcome! If you have encountered unique Play Console edge cases, feel free to submit a pull request or open an issue.

See [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and submission process.

---

## License

This project is open-source software licensed under the [MIT License](LICENSE).

---

**Maintained with care by [SAMFA Digital](https://samfa.online)**  
*Providing authentic Android closed-testing solutions, mobile QA, and custom software engineering.*
