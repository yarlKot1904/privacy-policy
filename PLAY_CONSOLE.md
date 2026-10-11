# Privacy policies and Play Console

Updated 2026-10-11. Contact: mdadev@yandex.ru.

## URLs

| App | Russian policy | English policy | App integration |
| --- | --- | --- | --- |
| Belarus Travel | https://yarlkot1904.github.io/privacy-policy/belarus-travel/ | https://yarlkot1904.github.io/privacy-policy/belarus-travel/en/ | Linked or bundled in app settings |
| Noizy | https://yarlkot1904.github.io/privacy-policy/noizy/ | https://yarlkot1904.github.io/privacy-policy/noizy/en/ | Linked or bundled in app settings |
| Flaggo | https://yarlkot1904.github.io/privacy-policy/flaggo/ | https://yarlkot1904.github.io/privacy-policy/flaggo/en/ | Linked or bundled in app settings |
| Resetly | https://yarlkot1904.github.io/privacy-policy/resetly/ | https://yarlkot1904.github.io/privacy-policy/resetly/en/ | Linked or bundled in app settings |
| Slimevar | https://yarlkot1904.github.io/privacy-policy/slimevar/ | https://yarlkot1904.github.io/privacy-policy/slimevar/en/ | Linked or bundled in app settings |
| Dices | https://yarlkot1904.github.io/privacy-policy/dices/ | https://yarlkot1904.github.io/privacy-policy/dices/en/ | Source code not supplied; add this URL inside the app before submission |

## Data safety preparation

App-local processing is not off-device collection in Google's Data safety definition. Advertising SDK transmission and developer support emails are separate from app-local content. Do not select “no data collected or shared” for a build that transmits advertising identifiers through Yandex Mobile Ads.

| App | On-device information | Off-device processing |
| --- | --- | --- |
| Belarus Travel | Visits, notes, custom places, selected photos, settings | Yandex advertising identifiers and ad request network/device data where advertising is enabled |
| Noizy | Microphone measurements; camera/audio recordings; timestamps, notes, calibration and device/audio metadata | Yandex advertising; manual export to a recipient chosen by the user |
| Flaggo | Learning answers, progress, XP, streaks, reminders | Yandex advertising; personalized targeting and SDK location tracking disabled in current code |
| Resetly | Sensitive habit/intimate-life journal, check-ins, relapse history, motivation, progress, reminders | Yandex advertising where configured; sensitive journal content stays local; personalization and SDK location tracking disabled |
| Slimevar | Game save, settings, local diagnostics (500 events, 64 run-duration entries), diagnostic export | Current game has no advertising SDK, external analytics, or INTERNET permission; external policy uses a browser |
| Dices / Кубики | Dice parameters and results; any locally retained preferences/history | Yandex advertising, according to the owner's description; no source/binary audit performed |

Google's and Yandex's guidance must be checked against the actual released binary and every active Play build/region. Current source does not establish what every previously released build transmits. Do not mark SDK collection optional solely because personalized ads can be declined: Noizy still requests advertising for both choices. Do not declare a global third-party deletion mechanism as implemented merely because an email is listed; verify the developer/provider process before answering that field. No numeric provider retention period is asserted here because it is controlled by Yandex.

## Submission steps

1. Use the app-specific public HTML URL in Play Console → App content → Privacy policy. The English page can be used as the listing URL.
2. Complete Data safety for each package using the actual distributed binary, including integrated SDK behavior. The table above is an inventory, not an automatic Play Console submission.
3. Confirm the displayed app name matches the policy. Rename the Dices/Кубики pages when the store name is finalized.
4. Rebuild apps after the source changes; already-installed APK/AAB files do not receive new embedded policies automatically. This task publishes the website and changes source; it does not upload app releases to stores.
5. Slimevar currently has no production advertising SDK. Update its policy and Data safety before shipping real Yandex advertising.
6. Dices source was not supplied. Its policy is based on the owner's description; add the policy inside the app and verify the actual SDK/consent configuration before submission.

## Official requirements

- [Google Play User Data](https://support.google.com/googleplay/android-developer/answer/10144311?hl=en)
- [Google Play Data safety](https://support.google.com/googleplay/android-developer/answer/10787469?hl=en)
- [Yandex Mobile Ads SDK Data safety](https://ads.yandex.com/helpcenter/en/dev/android/app-privacy-android)
- [Yandex Privacy Policy](https://yandex.com/legal/confidential/)

## Hosting

Static HTML; no JavaScript, cookies, forms, third-party fonts, or build dependencies. Publish main at /(root) through GitHub Pages. Root RU/EN pages are an app index, not a universal policy to paste for every app. .nojekyll keeps publication buildless.

