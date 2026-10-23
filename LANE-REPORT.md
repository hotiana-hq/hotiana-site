# Privacy and account-deletion lane report

Date: 23 October 2026. Scope: `privacy/index.html`, `delete-account/index.html`, and `support/index.html` in this worktree.

The approved app policy in `_lane-refs/APPROVED-PRIVACY-POLICY.md` takes precedence over yesterday's draft and `_lane-refs/EVIDENCE.md`. The founder's decisions in the task supply today's operational facts. No git commands, publishing, deployment, or external messages were performed. Reference copies were read and left untouched. Existing stylesheets, navigation, fonts, responsive tables and page structure remain in use; no CSS changes were made.

## Result

- Resolved all 60 original owner spans: privacy 47, delete-account 13, support 0. All three pages now show **Last updated 23 October 2026**.
- Privacy and deletion contact: **privacy@hotiana.ca**. Contacts are email-only. Support retains **uzair@hotiana.ca** for general help and directs privacy/deletion requests to the approved privacy address.
- The deletion page presents exactly two account-deletion routes: **Settings > Account > Delete my HOTIANA account and data**, and email **from the account's email address**. Local erasure and revoking one AI are explained separately as controls that do not delete the account.
- In-app deletion removes profile fields/revokes access immediately when processed; remaining account records are purged within 7 days. Email requests are completed within 30 days of the request. Backups expire within 30 days after deletion from the database. Email deletion does not erase a phone's local storage.
- Care content is removed throughout. Vantage has only the approved notice that it is not yet available on Google Play and will be added to the policy before availability.
- Audience is 18+. Action record and phone-link descriptions are unconditional because the founder confirmed they are in the build.
- Firestore location is Toronto (`northamerica-northeast2`), with encrypted daily backups retained 30 days and 7-day point-in-time recovery. Cloud Logging retention is 30 days.

## Evidence used for retained detail

| Detail | Authority |
| --- | --- |
| Android app scope, publisher, vault release approval, recipients, permissions, service retention and deletion commitments | Approved policy, corresponding sections |
| Live identity deletion and AI-reply intake | Founder: deployed 23 October at 01:09; supersedes the old deployment status in EVIDENCE A/B/G |
| Purge scheduling | Founder: daily at 03:17 Toronto; supersedes EVIDENCE B's unscheduled status. Schedule is recorded here, not exposed as a product instruction. |
| 10-minute sign-in requirement, confirmation, pre-account local-data choice, clear local storage only after server confirmation | EVIDENCE B and D |
| Immediate revocation, Google identity detachment, device-name scrubbing, purge categories and two-year one-way installation code | Approved deletion section; EVIDENCE B |
| AI consent permission groups, grant list/revoke behavior, refusal of next action, device listings within seconds | Approved bridge section; EVIDENCE B/C/D |
| Relay receipt lifetime and metadata-only logs | Approved bridge/retention sections; EVIDENCE C |
| 90-day/10,000-action encrypted local record, no content/arguments/numbers/keys, export/delete and backup exclusion | Approved local-data section; EVIDENCE D2. PC/TV copies are not claimed. |
| Today's encrypted notification history (400 maximum), cloud notification limits and private-access window choices | EVIDENCE F/G |
| Gemma processing on the phone, no cloud fallback, no model download in Play | EVIDENCE G |
| ElevenLabs only, optional own ElevenLabs key | Approved cloud-voice section; EVIDENCE B/G |
| OpenAI web search, prohibited query content, Mapbox errands and approximate location, weather rounding and update behavior | Approved services section; EVIDENCE B/F/G |
| Play does not start FCM, use Google Home APIs, send crash reports, request SMS/Call Log, background location or advertising ID permission | Approved Google Play services section; EVIDENCE G |
| Direct Tailscale computer link, signed requests, Desk clipboard/microphone, sign-in codes, alert metadata, phone-link notification/text/file limits and retention | Approved computer section; EVIDENCE E; founder confirms phone link ships |
| Report preview/device check, payload, local 50-report limit, no attached account, automatic 30-day deletion | Approved report/retention sections; EVIDENCE G; founder confirms intake live |
| Home YouTube/Google News widgets and DW/Al Jazeera/Bloomberg headlines | EVIDENCE G: components present with no Play gate found. Text describes loading content and makes no new cookie/advertising claims. |
| Play relay lifecycle, including possible background interruption | Approved bridge section; EVIDENCE H |

## Statements removed or replaced, and why

This inventory includes removed substantive claims and unresolved draft instructions. Rewording that preserves an evidenced claim is not a removal. Repeated statements in summaries, recipient tables, retention tables and footers are covered by the same entry.

| Removed statement(s) | Where | Reason / replacement |
| --- | --- | --- |
| “22 October 2026 (draft)” and an unassigned effective date | Privacy | Approved policy is dated 23 October; one last-updated date now appears on each page. No separate effective date was invented. |
| Apple device editions are in development/not yet available; Apple test-group instructions and Apple-specific device examples | Privacy, support | Neither the approved Android policy nor EVIDENCE establishes these release-status claims. |
| The policy covers Windows Companion, all listed apps and all editions | Privacy | Approved scope is the Android app. Its optional computer connection remains described. |
| Windows Companion is a preview and not yet generally available | Privacy | Availability status is not established by the supplied references. |
| Vantage is available as a direct-install test build; deletion steps apply to Vantage | Privacy, delete-account | Replaced with the approved Google Play nonavailability notice. Vantage is outside the current approved policy scope. |
| Vantage accessibility implementation: strip, touch positions, notification shade, no screen/event inspection or automated gestures, disclosure buttons, settings activation and local-only processing | Privacy | Removed the whole Vantage accessibility section; approved policy defers Vantage coverage until availability. EVIDENCE F calls it carried-over test-build content. |
| The “Two editions” comparison and direct-install SMS/default-phone, maps, crash-report and problem-reporter promises | Privacy | Current policy covers the approved Android app. Most of these detailed test-build data flows are not substantiated by EVIDENCE. |
| HOTIANA works without an account; sign-in is needed for computer/bridge and signed-in-tester cloud features | Privacy, delete-account | The supplied references do not establish every part of this feature-eligibility statement. Deletion guidance no longer depends on it. |
| Beta sign-in is invitation-only, refuses other accounts without creating an account, and leaves everything else working | Privacy | EVIDENCE G establishes tester gating for web answers, not all of these sign-in/account-creation assertions. Approved policy does not impose this blanket beta qualification. |
| The app loads the profile picture from its returned link, normally Google | Privacy | Fetch behavior and its recipient are not established in EVIDENCE or the approved text. Account/profile-picture-link processing remains disclosed. |
| Widget entries include dates/timers/document links; deleting widget settings leaves linked files | Privacy | These specific storage/erasure claims lack supplied evidence. Settings remain disclosed as local. |
| The action record covers PC/TV/relay copies or actions requested by computers and TVs | Privacy | EVIDENCE D2 says PC/TV/relay copies are design-only. Kept the approved description of connected-AI actions on this phone. |
| Action record and phone link may not ship or are unmerged | Privacy, delete-account | Founder confirmed both are in the build. Removed conditional wording and retained evidenced behavior. |
| Speech models are downloaded through Google Play after consent and Google sees only a normal download | Privacy, recipient table | EVIDENCE G says the requested speech_pack is undefined. Removed the unsupported working-download/recipient claim. |
| Installed speech recognition/spoken voice behavior and dictation's system recognizer/on-device preference/possible online fallback | Privacy | These exact assertions are not established by the approved policy or EVIDENCE. Kept approved local wake-word/routing/vault processing and evidenced Gemma behavior. |
| A future model download must name a provider such as Hugging Face | Privacy | Draft instruction for a feature that is not present; Play does not download the model. |
| Identity error logs contain only error type, code location, route and request ID | Privacy | Exact identity error-log allowlist is not established in EVIDENCE. Approved request metadata and evidenced relay logging remain. |
| Request logs necessarily include the Android version and request duration | Privacy, delete-account | Simplified to the approved time/address/status/IP/app-identifier disclosure; no need to retain unverified identity-log field detail. |
| TV launch distribution needs confirmation | Privacy | Removed distribution speculation. Approved policy and EVIDENCE B/C support TVs in grants/device records without asserting TV availability. |
| Direct-install relay stays connected in background and after restart | Privacy | EVIDENCE H supports it, but it describes test builds outside the approved app policy's present scope. Kept the Play lifecycle detail. |
| Device PIN is usable only when biometrics are unavailable | Privacy | Approved policy allows fingerprint, face or device PIN without that restriction. |
| Share-sheet AI handoff, authenticated selected context, sending in the other app, no automatic reply reading | Privacy, recipient table | Not established by EVIDENCE or the approved policy. Bridge and explicitly approved vault-release flows remain. |
| Cloud voice receives personality settings, automatic conversation-start context/caller identity, previous conversation history, calendar/reminder/contact results and direct-install call/message/location results | Privacy | Supplied evidence substantiates cloud audio/text and notification results, not all listed payloads. Kept the approved audio/conversation disclosure and evidenced notification limits. |
| Private reads bypass the lock when the phone has no screen lock; all enumerated private reads share the exact unlock behavior; conversations continue on another screen | Privacy | These precise behaviors are not established in the supplied references. Kept the evidenced private-access window options without the unverified bypass/continuation claims. |
| An unresolved separate notification-consent design must be decided | Privacy | Removed internal product/consent instructions. The current evidenced cloud-notification behavior remains described; no new consent mechanism is claimed. |
| An unused OpenAI voice option exists in the app | Privacy | Approved cloud voice is ElevenLabs; the option is not used by the Play edition (EVIDENCE G). |
| Provider retention is unresolved and zero retention is recommended | Privacy | Replaced provisional discussion with approved wording that ElevenLabs handles data under its own policy. No zero-retention claim is made. |
| Account identity is never sent to OpenAI and requesting nonstorage is no guarantee about its own logs | Privacy | Used the approved, narrower statement that question text rather than name/email is sent and nonstorage is requested. EVIDENCE B supports the request contents; no additional provider-log claim is needed. |
| Web answers are restricted to signed-in testers and include a specific search/news/translation/definition list | Privacy | Approved policy describes signed-in general-knowledge web questions. Used that scope without expanding eligibility claims from older evidence. |
| MCP connection IDs/names/addresses/privacy tiers/schedules/tools/Home presentation sync to the account and are erased with it; tokens are excluded from that sync | Privacy, delete-account | EVIDENCE B says the account-settings route is not live. Removed the paragraph and matching retention/deletion rows; settings remain local under the approved policy. |
| MCP revocation depends on the provider | Privacy | Used the approved disconnect commitment: revoke the token and delete it from the phone. |
| PC agents, Claude Code/Codex/OpenClaw instructions/output, completion notifications and provider processing | Privacy, recipient table | EVIDENCE E says Play hides the agents screen and does not establish every alternate route/provider. Approved computer policy covers direct phone/computer transfers, not this test-build feature. |
| Computer host-name/listener implementation and claim HOTIANA adds no second encryption layer | Privacy | Simplified to approved Tailscale encryption and direct routing; retained signed-request detail supported by EVIDENCE E. No universal transport encryption claim is added. |
| Directions always open the default maps app; test-build Mapbox maps/routes/tiles and map diagnostics | Privacy, recipient table | These full data-flow claims are not established by the supplied evidence. Retained approved place search and evidenced Play errand use, with approximate location and language. |
| FCM in direct-install builds wakes calls/messages and Google holds an installation registration token | Privacy, recipient table | EVIDENCE G establishes that Play does not start FCM, not the claimed direct-install behavior. |
| AI report sending is off, intake is undeployed, or sending depends on an unspecified build switch | Privacy, delete-account | Superseded by founder confirmation that intake is live and the approved policy's sending flow. |
| Reports can be exported to any chosen app | Privacy | Exact export behavior is not established in EVIDENCE G; local saving and sending remain. |
| Report service refuses any report carrying a name/email/account, never stores a network address, and requires operator identity confirmation | Privacy | EVIDENCE G substantiates rejecting Authorization/Cookie, not rejection of every possible personal value in reply text. Application intake hashing does not negate approved Cloud request logs with IP addresses. Removed the overbroad refusal/nonstorage wording and internal staffing instruction; retained the no-attached-account payload and preview caution. |
| Automatic crash-report payload (device/stack trace/recent steps/start time) and manual problem-report screenshots/recordings/logs/state go to the developer's computer | Privacy | Not substantiated in EVIDENCE or the approved policy; only the Play no-crash-report behavior is retained. No unsupported retention period was filled in. |
| Direct-install Google Home opt-in/House behavior and homes/rooms/devices/command data | Privacy, recipient/retention tables | Approved policy states Play does not include Google Home APIs. Detailed test-build flows are outside scope and not substantiated here. |
| Home media providers may set cookies/show ads; direct-install browser/media/TV requests | Privacy | EVIDENCE G supports present Home content but not all cookie/advertising details or test-build data flows. Kept Home providers without those new assertions. |
| TLS for Care/report/crash-report paths as part of an expanded encryption promise | Privacy | Used the approved encryption wording: identity and relay TLS, own-computer Tailscale encryption. Report intake is on the identity service; no broader connection guarantee is made. |
| All Care descriptions: invitation/family support, Care key/storage, AI readback/confirmation, request text/source/key/HTTPS desk transfer, human follow-up, health information, recipients and third-party deletion | Privacy, delete-account | Founder explicitly says Care is OFF in the Play build and to remove it. Removed its section and every summary/table/deletion reference. |
| Every contacted server sees ordinary network information | Privacy | Replaced this blanket third-party claim with the approved concrete service request-log disclosure and named recipients. |
| Detailed default-phone/default-message permissions and test-build SMS/MMS/attachments/call-log handling | Privacy | Outside current approved scope and not sufficiently substantiated by supplied evidence. Play's lack of SMS/Call Log access remains explicit. |
| Calls/texts always use prefilled default apps; exact-alarm/reminder permission details | Privacy | Supplied evidence does not establish these complete interaction/permission claims. Used the approved optional permission list. |
| Sign-in and removed-device record details remain indefinitely until account deletion; grant records remain until 30 days after scheduled expiry even if revoked earlier | Privacy, delete-account | Approved retention text wins: session lifetime, device enrollment and sign-in history follow the approved table; grant record is deleted 30 days after access ends. Removed the conflicting early-revocation extension. Purge categories remain evidenced. |
| Expired counters/other records have specific live Firestore TTL policies that still need confirmation | Privacy, delete-account | Used approved retention commitments (counters at most 24 hours, reports 30 days, sign-in history 90 days, grants 30 days after ending). No claim of independently inspecting live TTL configuration. |
| Deletion is switched off/unavailable on the serving revision; purge is unscheduled; do not publish until deployment/tests; email cannot work without a tool/manual database edits | Privacy, delete-account | Superseded by founder's live-deployment/scheduler decisions and approved email route. Removed notices, obsolete troubleshooting and internal deployment commands. No end-to-end test is claimed. |
| Email must have a particular subject, requires another user confirmation before the clock starts, and promises completion notification | Delete-account | Approved route requires the account email address and a deletion request, with completion within 30 days. No extra subject, user-response gate or notification promise is added. |
| Email uses exactly the in-app timetable without a fixed deadline | Privacy, delete-account | Now explicit: email completion within 30 days of request; backup expiry within 30 days after deletion. In-app remaining records purge within 7 days. |
| A general exception allows retention of anything required by law, with an individualized notice | Delete-account | No such exception/notice is in the approved policy or supplied evidence; removed rather than inventing retained categories. |
| No account means only logs/counters remain and everything else is on the phone | Privacy, delete-account | Sent reports carry no account and remain for 30 days. Removed the overbroad “only” claim and kept local erasure guidance separately. |
| HOTIANA contains no advertising/analytics tools and YouTube can show ads | Privacy | Approved policy establishes no sale, no advertising use and no ad tracking. Evidence establishes no AD_ID permission, but not a full SDK/analytics inventory or YouTube ad behavior. |
| eSpeak NG/FFmpeg notices are listed in the app; GPL/source/build licensing review and publish-notices instruction | Privacy | EVIDENCE F supports components, not completion/accuracy of notices or resolution of licensing obligations. Removed the section rather than implying those checks are complete. |
| “Intended for adults” while only excluding children under 13; unresolved Play target-age choice | Privacy | Replaced with approved audience: people aged 18 and over, not directed at children. |
| Unassigned mailing-address fields and company city/province/country footer location | Privacy, delete-account, support | Founder requests email-only contact and no postal address. Company name remains; no address invented. |
| General support email is also the privacy contact | Privacy/delete-account footers, support introduction | Privacy/deletion now use privacy@hotiana.ca. General help keeps its existing address without representing it as the privacy intake. |
| Owner requests to change Play Data safety declarations, verify release metadata or confirm reachable panels | Privacy, delete-account | These are internal preparation notes, not policy statements. Approved publisher/build decisions and EVIDENCE G resolve site text. No Play Console changes or release audit are claimed. |

## Verification

- Static HTML parsing passed for all three files: balanced tags, unique IDs, no owner class tokens or `[OWNER:` markers, one correct last-updated date, and the approved privacy email.
- All internal links and fragment targets resolve. No page links to `_lane-refs/`.
- Content checks passed: no Care, stale deletion-off/unscheduled/undeployed notices, draft labels or mailing-address placeholders. Exactly two numbered account-deletion routes; exact in-app menu path, account-email sender requirement, 30-day email deadline and backup expiry are present.
- Exact literal `class="owner"` counts are **0 for privacy, 0 for delete-account, 0 for support**, additionally checked through parsed class attributes.
- The installed GNU grep executable could not start in this environment (Windows process status `3221225794`, no count output). The requested literal count was therefore verified with Python using the same literal pattern. This is a tool-launch limitation, not a page-content failure.
- No browser rendering or live account-deletion/intake test was performed. Deployment and scheduler status are founder-supplied facts. The edits validate static policy content and HTML structure, not service behavior.

Changed deliverables: the three requested HTML pages and this report. `style.css`, the home page and `_lane-refs/` were not edited. MASTER retains responsibility for committing, preparing the PR and removing reference copies before commit; nothing is published by this lane.
