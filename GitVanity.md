# Privacy Policy

Last updated: June 7, 2026

GitVanity ("the app") is published by Alsatian Consulting. This policy explains what data the app handles and how it is used.

## Summary

- No account registration is required.
- No analytics, crash reporting, or advertising SDKs are used.
- No personal data is sold or shared with third parties.
- All GitHub data fetched by the app is cached locally on your device only.

## Information We Collect

GitVanity does not collect personal information for analytics, advertising, profiling, or remote account management. The app does not operate its own cloud backend.

## Information Processed On Device

To perform requested actions, the app processes data you explicitly provide or that GitHub returns in response to your requests:

- The GitHub personal access token you enter
- Repository names, descriptions, and metadata you choose to add to your watch list
- GitHub API responses including traffic metrics, commit activity, contributors, languages, community profile data, and forks for repositories you select

All of this data is processed and stored locally on your device. None of it is transmitted to Alsatian Consulting or any server other than GitHub's API.

## Token Storage

The GitHub personal access token you provide is stored using Android's `EncryptedSharedPreferences` with AES-256 encryption, backed by the Android Keystore system. The token is used solely to authenticate requests to the GitHub REST API (`api.github.com`) on your behalf and is never transmitted to any other destination.

## Local Caching

API responses from GitHub are cached in a local Room database on your device. Cached data is displayed when the network is unavailable or a request fails. Cached data remains on your device until you remove the corresponding repository from your watch list or uninstall the app.

## Network Use

GitVanity communicates exclusively with the GitHub REST API (`api.github.com`) to retrieve repository data. All network requests are authenticated using the token you provide. No other outbound connections are made.

## Permissions

GitVanity requests only the `INTERNET` permission. The app does not request access to your camera, location, microphone, contacts, or storage.

## Third-Party Services

GitVanity uses the GitHub REST API to retrieve data. Your use of the GitHub API is subject to [GitHub's Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement) and their Terms of Service. GitVanity has no affiliation with GitHub.

## Children's Privacy

GitVanity is not directed to children under 13 and does not knowingly collect personal information from children.

## Changes to This Policy

This privacy policy may be updated from time to time. Updates will be posted in this document with a revised "Last updated" date.

## Contact

Publisher: Alsatian Consulting  
Email: geoff@alsatian.consulting  
Website: https://alsatian.consulting
