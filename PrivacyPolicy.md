# Perspicio
Last updated October 31, 2026

Perspicio ("the app") is a study application operated by Airwulf LLC. This policy describes what we collect, why, and the choices you have.

What we collect
Account information — name, email address, username, date of birth, and a hashed password when you create an account. We use your date of birth to confirm you are at least 13 and to choose ad settings for your age (see Advertising identifiers below).
Ad measurement — in the iOS app, RevenueCat receives records of ads loading, being displayed, being tapped, or failing to load; rewarded-ad offers being shown or accepted; and rewards reported as earned by the ad SDK. These records include the ad format and placement (where it appears in the app), ad unit and network, mediation provider, impression ID, timestamps, and, when available, the revenue amount and currency or load-error details. They are linked to the same RevenueCat app user ID used for purchases, which is associated with your Perspicio account when you sign in. We use them to measure ad performance and revenue alongside subscriptions, not to personalize ads. This measurement does not itself collect the advertising identifier (IDFA), and we do not add your search queries or study content to these events. It does not verify or grant an AI unlock: our server separately verifies rewarded ads with Google AdMob as described below.
Sign-in — our servers check email-and-password sign-in themselves. Google Firebase Authentication handles Sign in with Apple and Google, and when you create an account with an email address a matching sign-in record (your email address, name, and password) may also be created there. If you use Apple or Google sign-in, Apple or Google and Firebase process it and we receive an identity token that includes your email address; Firebase keeps a sign-in record for that Apple or Google identity even if no Perspicio account matches it.
Study content — decks, flashcards, notes, goals, media items (links, pasted text, transcripts, summaries, and quizzes), question sets, and tutor conversations you create. Synced content is stored on our servers so it follows your account across devices; question sets stay on your device.
Study activity — each question you answer and whether it was right, the topic it belongs to, and your reviews, retests, quiz results, and streaks are saved with your account. They power weak-area practice, retests, progress and readiness estimates, and recaps.
Reports and blocks — if you report a deck, a cohort member, or an error in a question or card, or block a cohort member, we store the report (who made it, what it is about, and any reason or note you type) so we can review it.
Search history — recent search queries and saved result cards are stored on your device so you can return to them. Explore sends queries to our server and Brave to return results; if you choose “More results on Google,” the query is sent to Google instead. Our server keeps short-lived, in-memory search caches: web results for up to one hour and image results for up to 24 hours. When AI features are on, AI search sends your query to Google (which uses Google Search to find sources) and, where available, to Brave; image search sends your search words, through our server, to Wikimedia Commons. Search history is used to provide search features, not for advertising or cross-app tracking.
Usage and diagnostics — Google Firebase Analytics records the screens you open (the screen's address inside the app, which can include the ID of an item such as a deck or a media item) and events such as flashcard reviews, finished study sessions, goals created, imports, flashcard generation, and tutor hand-offs (with the topic and deck involved). Our own servers also record a short list of in-app events, such as upgrade and checkout steps, practice and retest steps, and cohort and streak actions, against your install ID and, if you are signed in, your account. Crash and error reports go to Sentry and Firebase Crashlytics; before a report goes to Sentry, fields that hold names, email addresses, and card content are removed, and so are email addresses found in text. AI feature usage is metered with your account for plan limits.
Install ID and IP address — in the mobile app, a random install ID is created on your device and sent with each request. We store it with push registrations, in-app usage events, and study activity, and, for about 48 hours, with rewarded-ad unlocks, and we use it with your IP address to limit abuse. Our servers see your IP address on every request. Rate limiting keeps the address and install ID in server memory, or in an external Redis service if we use one, for an hour or less after your last request by default; the address also appears in server logs, which can also hold your account ID and install ID; and if we switch on a captcha check at sign-up or password reset, the address is sent to the captcha provider (hCaptcha or Cloudflare Turnstile).
Push notifications — if you allow notifications and leave Announcements on in Office, we store a push token (issued through Apple and Google Firebase Cloud Messaging) with your account, together with the install ID, the platform, and the app and operating-system versions, so we can send you announcements from us. Turning Announcements off, or signing out, stops them on that device.
Advertising identifiers — the free tier shows ads served by Google AdMob. We request non-personalized ads. The advertising identifier is used only to limit how often you see the same ad, count ad views, and help prevent ad fraud. We do not use it to personalize ads or track you across other companies' apps or websites. Ad settings follow your age bracket, worked out from the date of birth you gave at sign-up: users under 18 get stricter handling. AdMob is sent that setting, not your date of birth.
Rewarded-ad records — if you choose to watch rewarded ads to unlock an AI action (a search, summary, quiz, set of flashcards, or learning path), we keep a record of that unlock (your account, which feature, and timestamps). To limit abuse we also keep, for about 48 hours, a scrambled (hashed) form of your IP address and your install ID (described above). Google AdMob receives a random code for the unlock, not your account details, so it can confirm the ads were watched. The unlock record is deleted after about 90 days or when you delete your account, and the note on your AI usage record that an unlock paid for an action is cleared after 97 days.
AI features and your choice
In the current version of the app, AI features are optional and stay off until you allow them. The first time you use one, the app explains what will be sent and asks. Your choice is recorded with your account, along with the date and the version of this notice you saw. You can change it at any time under Office → Privacy → AI features. Once you turn AI features off, nothing new is sent to AI services, except for the automated safety check OpenAI runs on a deck you choose to publish (see Safety checks below); results you already have stay, and importing, your own cards, and studying keep working.

Who receives your content. Two outside AI services process it for us:

Google — summaries, AI search and related-lesson search, study resources for questions you missed, the web-research part of study packs and web quizzes, the tutor's resource search, teach-back scoring, and automatic quality checks on generated flashcards and quiz questions, which see each card or question together with the part of your material it was made from.
OpenAI, through AI Integrations — quizzes; flashcards, including from photos and documents; explanations; analysis; learning paths and missions; the tutor and its lessons; reading questions from photos; voice transcription and read-aloud; deck tag suggestions; and answer diagnoses.
What is sent. Only what the feature needs: text, notes, documents, web pages, photos, and voice recordings you choose to use, with their titles; answers you ask to have checked; tutor messages, the recent conversation, and titles of items in your library; and your learning-style profile, reading level, and teaching-style settings when they personalize a result. We never add your name, email address, username, date of birth, or payment details, but anything you type or upload goes as you wrote it.

Safety checks. Text you type or upload for AI features is first checked by OpenAI's automated moderation service so harmful requests can be blocked, and what the AI writes back, including each reply from the tutor, is checked the same way before it is shown to you. We reach that service directly with our own OpenAI account, not through Replit AI Integrations. Image-search words and the contents of a deck you publish are checked the same way. A deck you publish is checked even when AI features are off, because publishing is not behind the AI choice: its name, description, tags, and cards are sent to that service before the deck goes live.

Background processing, only while AI features are on. These happen on their own, without a separate tap for each one:

A summary and starter flashcards, made right after you import a link or a file.
Once a day, the tutor's short notes about questions you missed are condensed into a few study notes.
Extra Fix-it cards on a topic when the question bank runs short (the topic only).
Study resources for questions you missed, searched for automatically when you open a session review or the results of a question set.
An explanation of the mistake behind a wrong answer, made right after you miss a question in a retest.
A new set of missions made from your learning goals, at most once a day.
Read-aloud of the tutor's replies, when auto-play is on in your settings.
The tutor's first message, sent for you when a learning pathway hands off to the tutor and automatic sending is on in your settings.
How long it is kept. Results generated from your own content (summaries, flashcards, analyses, explanations, and teach-back scores) may be cached under your account for up to 30 days, are never shown to anyone else, and are deleted with your account. Study packs are generated from only the topic or item title you enter, and answer diagnoses from only a practice question, so the same result may be shown to other users who ask the same thing: do not put personal details in a study-pack topic or item title. The AI services may keep requests for a limited time to detect abuse, as their own terms describe.

Training. Your content is used only to produce the result you asked for. We do not use it to train AI models.

AI notice version ai-2026-11. When it changes in a material way, the app asks you again.

Payments
Paid plans and in-app purchases are processed by our payment providers: Stripe on the web, and Apple (In-App Purchase) in the iOS app. We never see or store your full card details. In the iOS app, RevenueCat manages purchases and subscriptions for us: when you sign in, the app gives it your Perspicio account ID, and it receives your purchase information from Apple and tells us your plan.

What we store: your plan tier and subscription status; for Apple purchases, the product, its expiry date, and whether it will renew; a ledger of AI credit purchases, refunds, and the AI features credits were spent on; the date you bought ad removal, if you did; and, for Stripe, your Stripe customer ID and a synchronized copy of Stripe's records for your customer (such as subscriptions, invoices, charges, and payment methods), which can include your email address, billing details, and the card brand and last four digits.

Service providers
Besides the AI services, ad network, and payment providers named above, these companies process data for us:

Replit hosts our servers and database, and provides the AI Integrations service through which we reach OpenAI.
Google Firebase provides Apple and Google sign-in (Authentication), Cloud Firestore (which can hold synchronized copies of your account and study data), analytics, crash reports (Crashlytics), and push messages (Cloud Messaging).
Sentry receives error and crash reports.
Resend delivers our emails, so it receives your email address and the message, which can include your first name.
RevenueCat manages in-app purchases and subscriptions and measures iOS ad activity and revenue linked to the same app user (see Payments and Ad measurement).
YouTube (Google) plays videos inside the app through its embedded player, under Google's own privacy policy.
Brave returns Explore results, so it receives your Explore queries.
Have I Been Pwned checks the password you choose against known data breaches. It receives only the first five characters of the password's SHA-1 hash, never the password.
Redis — if we use an external Redis service for rate limiting, it holds the counters described under Install ID and IP address.
What other learners can see
Cohorts and duos — if you create or join one, its other members can see the display name you chose, your weekly numbers (cards reviewed, questions answered, accuracy, and streak), and an internal ID for your account that the app uses for its Report and Block buttons.
Published decks — a deck you publish to the marketplace, with its name, description, tags, and cards, can be viewed and imported by anyone, including people without an account. The marketplace does not show your name with a deck. You can unpublish a deck at any time from the deck's page; see Data retention and deletion for decks you leave published.
What we do not do
We do not sell your personal information.
We do not use your study content for advertising.
We do not use advertising identifiers to track you across other companies' apps or websites.
Data retention and deletion
Your data is retained while your account is active. You can permanently delete your account at any time from Office → Delete Account in the app. Deletion cancels any subscription billed through Stripe and removes your content from our systems, including cached AI results and your learner profile; copies may also remain in backups until those backups expire. Copies held in Google Firebase's sign-in and database services (Authentication and Firestore) are removed by an automatic process that retries until it succeeds, normally within an hour. We keep a deletion record for 30 days after the deletion finishes. It holds only an internal account number, dates, the Stripe customer ID (so the subscription can still be cancelled), the outcome of each deletion step, and the last error message, if there was one. Subscriptions billed through Apple cannot be cancelled by us — cancel them in your Apple ID subscription settings, otherwise Apple will continue to bill you after the account is deleted.

Deleting your account does not remove everything:

Decks you published to the marketplace stay available to other users, without your account attached, unless you unpublish them first.
AI usage records (the feature, time, token counts, and estimated cost of each request) and in-app usage events stay with your account ID removed. Usage events can still carry the random install ID. We keep both without a fixed deletion date.
Server logs, which can include account IDs, install IDs, and IP addresses, are not edited when you delete your account.
Records held by other companies follow their own policies. We do not send Apple or RevenueCat a deletion request, so RevenueCat's purchase and ad-measurement records are not automatically deleted when you delete your Perspicio account. Their retention follows RevenueCat's policies. Nothing is removed from what Firebase Analytics, Crashlytics, Sentry, or Resend have already received. Stripe, and the copy of its records we keep in our own database, may keep customer, invoice, or payment records after your Stripe customer is deleted. A Firebase sign-in record made by an Apple or Google sign-in that matched no Perspicio account is not removed either.
Email
We send transactional emails (a welcome message, password resets, and a notice if someone tries to sign up with an address that already has an account) and product emails: a suggestion to upgrade, sent at most once a month to people who have reached a plan limit in more than one month, and a weekly progress recap. Product emails have a one-click unsubscribe link, and the Upgrade emails switch under Email preferences in Office turns off all of them, the recap included. Our email provider, Resend, delivers them.

Children
Perspicio is intended for users aged 13 and older. We ask for your date of birth when you create an account and do not create accounts for people under 13. We do not knowingly collect personal information from children under 13.

Changes
We will update this page when our practices change and revise the date above.

This website
This website is for information only and has no accounts or forms. It is hosted by Github, which may log technical data such as your IP address and browser type and may give us aggregate visit statistics. This section covers the website only; the rest of this policy covers the Perspicio app.

Contact
Airwulf LLC · airwulf22@gmail.com
