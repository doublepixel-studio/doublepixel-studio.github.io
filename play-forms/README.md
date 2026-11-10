# Play Console form answers

Google Play's Data safety answers for the games on this site, as CSV. Play Console's Data safety page has
**Export to CSV / Import from CSV**; the file is validated on import (a bad value is refused with the exact question
id, and nothing is changed). The question ids are stable, so a file made from another game's export imports as is.
Older games keep theirs in `barsagivv/arclogic-studio/play-forms/`.

## data-safety-toyflyers.csv

Toy Flyers (`com.doublepixel.toyflyers`), 2026-11-09, matching
<https://doublepixel-studio.github.io/toyflyers/privacy-policy.html>. Made from Quack Blast's file (same 782 rows and
ids), with every answer set again. **Filed on 2026-11-10** through the API (`POST applications/<package>/dataSafety`,
HTTP 204). Play refused the first try with "You cannot answer PSL_HAS_OUTSIDE_APP_ACCOUNTS": when account creation is
OAuth that optional question must stay empty, so its value was removed from this file.

- Encrypted in transit: yes. Account creation: OAuth (optional Sign in with Google / Apple; the guest account is
  anonymous). Account deletion URL and data deletion URL: `toyflyers/delete-account.html`. Data sold: none.
- Collected only (Firebase is a service provider, not "shared"), not ephemeral:
  - Personal info: Name (the nickname, and the name Google or Apple shares): optional; App functionality, Account
    management. Email address (from Google or Apple): optional; Account management. User IDs (account id, friend
    code): required; App functionality, Account management.
  - Financial info: Purchase history (the store's transaction id, kept to prevent double use): optional; App
    functionality, Fraud prevention.
  - App activity: Other actions (cloud save, profile, trophies, arena, leaderboards, weekly league, friends, presence,
    race presses, shared replays): required; App functionality.
- Collected and shared (AdMob), required, not ephemeral; purposes Analytics, Fraud prevention, Advertising (collected
  and shared):
  - Location: Approximate location (AdMob, from the IP address).
  - App info and performance: Diagnostics.
  - App activity: App interactions (Firebase Analytics events, ad interactions).
  - Device or other IDs (advertising id with consent, Firebase app instance id, FCM device token): collected also for
    App functionality and Developer communications (push notifications).
- Not declared: crash logs (no crash reporter), precise location, contacts, messages (no chat: six preset emoji faces
  only), photos, files.
