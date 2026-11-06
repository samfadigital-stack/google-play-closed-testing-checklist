# How to Answer the Google Play Production Access Questionnaire

When your 14-day closed testing period concludes with at least 12 continuously opted-in testers, Google Play Console invites you to apply for production access. 

As part of the application, Google requires you to complete a structured questionnaire about your testing methodology, feedback collected, and app improvements. Google's review team uses these answers to evaluate whether your testing was genuine.

---

## Question 1: How did you recruit your testers?

### ❌ Ineffective Answers to Avoid:
- *"I invited friends and family."*
- *"I shared the link on social media."*
- *"Used an online service."*

### ✅ Effective Framework:
Explain your target user profile, device diversity, and the communication channels you used to coordinate testing.

> **Example Framework:**  
> *"We recruited a cohort of 16 participants across multiple physical Android hardware devices to evaluate compatibility across diverse OEM skins and Android OS versions (including Samsung Galaxy One UI on Android 13/14, Google Pixel on Android 14, Xiaomi HyperOS on Android 13, and OnePlus OxygenOS). Testers were onboarded via a dedicated Google Group with explicit instructions to install the build from the closed track, test authentication and offline modes, and submit feedback on UI responsiveness and crashes."*

---

## Question 2: What feedback did you receive from testers during closed testing?

### ❌ Ineffective Answers to Avoid:
- *"Everything worked great."* (This is an immediate red flag for review teams, as all pre-release software has edge cases).
- *"No bugs were found."*
- *"Positive reviews only."*

### ✅ Effective Framework:
Provide 2 to 4 concrete, actionable examples of usability friction, layout defects, or edge-case bugs identified by your testers.

> **Example Framework:**  
> *"Testers provided several specific observations:  
> 1. On lower-resolution devices (such as 720p screens), the checkout confirmation button partially overlapped the bottom navigation bar.  
> 2. On Android 14, two testers reported that the notification permission prompt dismissed unexpectedly on first app launch.  
> 3. Testers noted that when launching the app in weak network conditions (3G/high latency), the initial dashboard displayed an empty screen rather than a clear loading skeleton state."*

---

## Question 3: What changes or improvements did you make based on tester feedback?

### ❌ Ineffective Answers to Avoid:
- *"None needed, the app was already complete."*
- *"Fixed some minor stuff."*
- *"Will fix in production."*

### ✅ Effective Framework:
Directly tie your answers to the updates (`versionCode`) you shipped during the 14-day closed testing cycle.

> **Example Framework:**  
> *"Based on tester feedback, we released update v1.0.1 (versionCode 2) on Day 6 of the closed testing period:  
> 1. Refactored the checkout view to use a responsive, scrollable container, resolving button clipping on smaller display resolutions.  
> 2. Implemented an explicit permission rationale dialog prior to requesting runtime permissions on Android 13+.  
> 3. Added a lightweight skeleton loading animation and cached placeholder states to improve perceived speed on slower data connections.  
> Subsequent feedback from our testing cohort confirmed these issues were resolved with no regressions."*

---

## Additional Review Tips

1. **Be Honest and Factual:** Google's internal telemetry records crash rates, ANR rates, and opt-in counts. Ensure your answers align with actual Console metrics.
2. **Ship an Update:** Rolling out at least one minor update during testing proves active bug triage.
3. **Check Policy Compliance:** Confirm your Privacy Policy URL is accessible and your Data Safety disclosures match your app's actual permissions.

---

*Guide provided by [SAMFA Digital](https://samfa.online) &mdash; Google Play Closed Testing Services & Android QA.*
