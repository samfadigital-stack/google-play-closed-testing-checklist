# How to Answer the Google Play Production Access Questionnaire

When your 14-day closed testing period concludes with at least 12 continuously opted-in testers, Google Play Console invites you to apply for production access across three structured sections (~8 questions total) covering your closed test, your app, and production readiness.

> **Important:** Treat every example below purely as a *structural framework*. Never copy-paste placeholder text or numbers into Play Console—Google cross-checks written claims against your real Play Console opt-in telemetry, release uploads (`versionCode` history), and Android Vitals metrics. For detailed question-by-question guidance, see our [Production Access Questionnaire Answers Framework](https://samfa.online/guides/google-play-production-access-questionnaire-answers/).

---

## Question 1 (Section 1): How did you recruit and onboard your testers?

### ❌ Ineffective Answers to Avoid:
- *"I invited friends and family."*
- *"I shared the link on social media."*
- *"Used an online service."*

### ✅ Effective Framework:
Explain your real recruitment channels, cohort size, physical-device diversity, and how easy or challenging opt-in/onboarding was across invited accounts.

> **Template Framework (Replace Brackets With Your Real Testing History):**  
> *"We recruited `[number]` participants across distinct physical Android devices (for example, `[list the actual phone models, OEM interfaces, and Android OS versions your testers used]`) to test our app's core journeys before public release. Testers were onboarded via `[your actual channel, e.g., our developer Google Group / Email List]` and guided to accept the Play Store closed-track opt-in, test `[core screens/onboarding/offline handling]`, and share bug notes."*

---

## Question 2 (Sections 2 & 3): What feedback did you receive from testers during closed testing?

### ❌ Ineffective Answers to Avoid:
- *"Everything worked great."* (Pre-release builds nearly always uncover layout, copy, or edge-case issues).
- *"No bugs were found."*
- *"Positive reviews only."*

### ✅ Effective Framework:
Summarize 2 to 4 genuine observations reported by your actual testers—whether layout sizing, onboarding confusion, permission prompts, or network error states.

> **Template Framework (Replace Brackets With Your Real Observations):**  
> *"Testers reported `[number]` specific items during our 14-day closed test:  
> 1. `[UI/layout detail, e.g., keyboard or compact-screen overlap on Screen X]`.  
> 2. `[Permission/auth edge case, e.g., dialog copy or OAuth redirect behavior on Android Version Y]`.  
> 3. `[Network/data handling note, e.g., missing loading or offline retry state when loading Screen Z]`."*

---

## Question 3 (Section 3): What changes or improvements did you make based on tester feedback?

### ❌ Ineffective Answers to Avoid:
- *"None needed, the app was already complete."*
- *"Fixed some minor stuff."*
- *"Will fix in production."*

### ✅ Effective Framework:
Directly tie your written summary to actual release updates (`versionCode`) uploaded to your closed track during the 14-day window and note how those fixes were verified.

> **Template Framework (Replace Brackets With Your Real Release Changelog):**  
> *"In response to tester feedback, we released `[your real versionName / versionCode]` on `[Day X]` of the closed testing window:  
> 1. `[Specific fix implemented for issue #1 and affected screen/component]`.  
> 2. `[Specific fix implemented for issue #2]`.  
> 3. `[Specific fix implemented for issue #3, e.g., added loading indicator and empty/offline fallback]`.  
> Subsequent closed-track checks confirmed those fixes behaved reliably with clean Android Vitals stability."*

---

## Additional Review Tips

1. **Be Honest and Factual:** Google compares written answers against actual Play Console telemetry (installs, retention, updates, and crash/ANR counts).
2. **Collect Structured Quality Evidence:** Review our [Google Play Tester Feedback & Testing Quality Guide](https://samfa.online/guides/google-play-tester-feedback-and-testing-quality/) before writing Part 3.
3. **Run the Full Pre-Submission Check:** Verify store assets, Privacy Policy, Data Safety, and closed-track continuity inside our [Google Play App Publishing Checklist](https://samfa.online/guides/google-play-app-publishing-checklist/).

---

*Guide provided by [SAMFA Digital](https://samfa.online) &mdash; Google Play Closed Testing Services & Android QA.*
