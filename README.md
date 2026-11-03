# Google Play Closed Testing Checklist: 12 Testers for 14 Days

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Platform: Android](https://img.shields.io/badge/Platform-Android-green.svg)](https://developer.android.com/)
[![Google Play Console](https://img.shields.io/badge/Google%20Play-Console-blue.svg)](https://play.google.com/console/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

A practical, open-source checklist for Android developers, indie creators, and development teams preparing for Google Play's closed-testing requirement.

For eligible personal developer accounts, Google requires **at least 12 testers to remain opted in continuously for at least 14 days** before the developer can apply for production access.

Created and maintained by [SAMFA Digital](https://samfa.online), sharing practical guidance for Android app testing and Google Play release preparation.

---

## Table of Contents

1. [Understanding the Requirement](#understanding-the-requirement)
2. [Phase 1: Pre-Testing Readiness](#phase-1-pre-testing-readiness)
3. [Phase 2: Closed Testing Track Setup](#phase-2-closed-testing-track-setup)
4. [Phase 3: Tester Onboarding](#phase-3-tester-onboarding)
5. [Phase 4: Testing and Feedback](#phase-4-testing-and-feedback)
6. [Phase 5: Production Access Preparation](#phase-5-production-access-preparation)
7. [Common Mistakes to Avoid](#common-mistakes-to-avoid)
8. [Useful Resources](#useful-resources)
9. [SAMFA Digital](#samfa-digital)
10. [Contributing](#contributing)
11. [License](#license)

---

## Understanding the Requirement

Since November 13, 2023, eligible personal Play Console developer accounts created after that date must complete a closed test before applying for production access.

The requirement is:

- At least **12 testers** must be opted in to the closed test.
- Testers must remain opted in continuously for **at least 14 days**.
- After completing the requirement, the developer can apply for production access.
- Google may ask questions about the testing process, tester feedback, and the app's readiness for production.

**Important:** Completing the 14-day testing requirement does not automatically guarantee production access. Google reviews the application and makes the final decision.

### Practical Recommendations

- Recruit a reasonable number of testers above the minimum to provide a buffer.
- Make sure testers use the correct Google accounts when joining.
- Share clear installation and opt-in instructions.
- Collect genuine feedback and document issues.
- Test important app features and fix problems where necessary.
- Review Google's latest official guidance before applying.

---

## Phase 1: Pre-Testing Readiness

Before creating a closed testing release, review your app's technical and operational readiness.

- [ ] Generate a signed Android App Bundle (`.aab`) using the release build configuration.
- [ ] Verify the app's package name and version information.
- [ ] Check the app's compatibility with supported Android versions and devices.
- [ ] Confirm that Google Play App Signing is configured appropriately.
- [ ] Test the main user journeys, registration, login, and essential features.
- [ ] Check for crashes, major bugs, and performance issues.
- [ ] Verify that the privacy policy is publicly accessible, where required.
- [ ] Complete the Data safety form accurately according to the app's actual data practices.
- [ ] Provide app access instructions or test credentials in Play Console if the app requires login.
- [ ] Review app permissions and third-party SDK usage.

---

## Phase 2: Closed Testing Track Setup

Follow the current Google Play Console workflow to configure your closed testing track.

- [ ] Open your app in Google Play Console.
- [ ] Navigate to the testing section and select **Closed testing**.
- [ ] Create a closed testing track.
- [ ] Configure the countries or regions where the test will be available.
- [ ] Add testers using an email list or Google Group.
- [ ] Review the tester list for incorrect or duplicate email addresses.
- [ ] Upload your signed `.aab` file.
- [ ] Add release notes explaining the purpose of the test.
- [ ] Review and roll out the release to the closed testing track.
- [ ] Wait until the release is available to testers before sharing the joining instructions.

*Note: Play Console labels and workflows may change. Follow the instructions currently displayed in your account.*

---

## Phase 3: Tester Onboarding

Inviting testers is not the same as having them opted in. Testers must complete the joining process.

### Share the Joining Instructions

- [ ] Copy the closed testing opt-in link from Play Console.
- [ ] Share the link with the invited testers.
- [ ] Ask each tester to open the link while signed in to the invited Google account.
- [ ] Ask them to select **Become a tester**.
- [ ] Direct them to the Google Play installation page.
- [ ] Ask them to install the app and follow the testing instructions.

### Verify Tester Participation

- [ ] Check the opted-in tester count in Play Console.
- [ ] Confirm that at least 12 testers have opted in.
- [ ] Keep a record of tester onboarding and feedback.
- [ ] Follow up with testers if they encounter installation or access problems.

### Device Compatibility

Where possible, include a useful mix of Android devices, screen sizes, manufacturers, and OS versions. This can help identify compatibility problems that may not appear on a single device.

---

## Phase 4: Testing and Feedback

Use the testing period to evaluate the app's functionality, usability, and stability.

### Suggested Testing Plan

**Initial Testing**

- [ ] Verify that the app installs and launches successfully.
- [ ] Test registration and login.
- [ ] Check the main navigation and important screens.
- [ ] Identify major crashes or blocking issues.

**Feature Testing**

- [ ] Test the app's main features and workflows.
- [ ] Check form validation and error handling.
- [ ] Test relevant network and offline scenarios.
- [ ] Review notifications and background functionality, if applicable.
- [ ] Check different screen sizes and device configurations.

**Feedback and Improvements**

- [ ] Ask testers to share genuine observations.
- [ ] Record bugs and usability problems.
- [ ] Prioritize issues according to severity.
- [ ] Fix relevant issues and verify the fixes.
- [ ] Release an updated build if an update is necessary.
- [ ] Keep a record of feedback and changes made during testing.

**Before Applying**

- [ ] Review the opted-in tester count.
- [ ] Confirm that the required continuous testing period has been completed.
- [ ] Review unresolved bugs and known limitations.
- [ ] Prepare accurate information about the testing process.

*The checklist above is a practical testing recommendation, not a statement that Google requires every activity on a specific day.*

---

## Phase 5: Production Access Preparation

After completing the applicable testing requirement, you can apply for production access through Play Console.

Prepare accurate and specific answers about your testing experience.

### Tester Recruitment

Be ready to explain:

- How you recruited your testers.
- Which channels or communities you used.
- How testers were invited to participate.

### Tester Feedback

Be ready to describe:

- What feedback testers provided.
- Which usability or technical issues they identified.
- What you learned from their experience.

### Changes Made During Testing

Explain:

- Which issues were addressed.
- What improvements were made.
- Whether an updated release was provided.

### Production Readiness

Describe:

- How the app's main features were tested.
- What issues remain, if any.
- Why you believe the app is ready for production users.

**Important:** Provide truthful answers based on your actual testing activity. Do not invent tester feedback, bug reports, or testing results.

---

## Common Mistakes to Avoid

| Mistake | Recommended Action |
|---|---|
| Inviting testers but not checking opt-in status | Verify the opted-in count in Play Console. |
| Sharing the link before the release is available | Wait until testers can access the release. |
| Using incorrect Google accounts | Give testers clear account instructions. |
| Providing unclear installation instructions | Share a simple step-by-step onboarding guide. |
| Ignoring tester feedback | Record and review genuine feedback. |
| Leaving major bugs unresolved | Investigate and fix important issues before applying. |
| Giving generic questionnaire answers | Explain your actual testing process and findings. |
| Relying on outdated policy information | Review Google's current official documentation. |

---

## Useful Resources

- **Google Play Testing Documentation:** [Set up an open, closed, or internal test](https://support.google.com/googleplay/android-developer/answer/9845334)
- **Production Access Requirement:** [Apply for production access](https://support.google.com/googleplay/android-developer/answer/14151465)
- **Android Developer Documentation:** [developer.android.com](https://developer.android.com/)
- **Google Play Console:** [play.google.com/console](https://play.google.com/console/)

---

## SAMFA Digital

[SAMFA Digital](https://samfa.online) provides practical support for Android app development, Google Play closed testing, and mobile app quality assurance.

### Our Services

- Google Play Closed Testing support
- Android app testing and QA
- Mobile app development
- Web development
- UI/UX design

### Closed Testing Packages

| Package | Testers | Duration | Price |
|---|---:|---:|---:|
| Starter | 12 | 14 days | $10 |
| Growth | 16 | 14 days | $50 |
| Scale | 20 | 14 days | $100 |

Package availability and service details are subject to confirmation.

**Need help with your app's closed testing?**

[Contact SAMFA Digital on WhatsApp](https://wa.me/923390667763?text=Hello%20SAMFA%20Digital%2C%20I%20need%20help%20with%20Google%20Play%20Closed%20Testing.%20Please%20share%20your%20packages%20and%20details.)

Website: [https://samfa.online](https://samfa.online)

Email: [samfadigital@gmail.com](mailto:samfadigital@gmail.com)

LinkedIn: [SAMFA Digital](https://pk.linkedin.com/company/samfa-digital)

GitHub: [samfadigital-stack](https://github.com/samfadigital-stack)

---

## Contributing

Contributions, suggestions, corrections, and feature requests are welcome.

If you have useful improvements or have identified outdated information, feel free to open an issue or submit a pull request.

See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

**Maintained by [SAMFA Digital](https://samfa.online)**

*Google Play Closed Testing Services & Android QA Solutions.*
