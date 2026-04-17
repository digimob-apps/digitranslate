# Privacy Policy — DigiTranslate

*Last updated: April 17, 2026*

DigiTranslate is a free browser extension developed by DigiMob Apps. This policy describes exactly what data the extension accesses, stores, and transmits — based on the actual source code of the extension.

---

## 1. Data We Do NOT Collect

DigiTranslate has **no backend server, no analytics, and no telemetry**. We do not collect, receive, or have access to any of your data. Specifically:

- No usage analytics (no Google Analytics, Mixpanel, Amplitude, or equivalent)
- No crash reporting services
- No user accounts or identifiers
- No advertising trackers or pixels
- No data is ever sent to digimob.app servers

---

## 2. Data Stored Locally in Your Browser

All data the extension stores remains in your browser and is never transmitted to us.

### 2.1 Synced across your browser instances (`chrome.storage.sync`)

The following settings are stored in your browser's sync storage, meaning they may be synced to other devices where you are signed into the same browser profile — by your browser, not by us.

| Data | Description |
|------|-------------|
| Target language preference | Your chosen translation language |
| Translation settings | Auto-translate, learning mode, hover mode toggles |
| TTS mode | Disabled, browser TTS, or ElevenLabs |
| ElevenLabs API key | Only if you configure ElevenLabs TTS (see section 4.3) |
| Keyboard shortcuts | Your customized hotkeys |
| Display preferences | Compact mode, confidence score display |
| Translation history | Last 100 translations (text, languages, source URL, timestamp) |

### 2.2 Stored locally only (`chrome.storage.local`)

| Data | Description |
|------|-------------|
| Glossary | Custom term pairs you define, with creation timestamps |
| Bookmarks | Translation pairs you save, with tags, notes, and source URL |
| Statistics | Total number of translations performed and total word count |
| Domain blocklist | Hostnames where you have disabled the extension |

### 2.3 Retention

- History is automatically capped at 100 entries; oldest entries are deleted when the limit is reached.
- All other data is kept until you clear it from the extension settings or uninstall the extension.
- Uninstalling the extension removes all locally stored data.

---

## 3. Data Transmitted to Third-Party Services

DigiTranslate sends data to third-party APIs to perform its core functions. We have no control over these services and do not receive copies of this data.

### 3.1 Google Translate (unofficial API)

**Endpoint:** `https://translate.googleapis.com/translate_a/single`

Every translation request sends:
- The text you selected or the page content being translated
- Source and target language codes

This API is used for all text translations and automatic language detection. It is an unofficial endpoint operated by Google. Google's privacy policy applies: [https://policies.google.com/privacy](https://policies.google.com/privacy)

### 3.2 Free Dictionary API (English only)

**Endpoint:** `https://api.dictionaryapi.dev/api/v2/entries/en/{word}`

When you look up a word definition, the word is sent to this public API. No personal information is transmitted. Service privacy policy: [https://dictionaryapi.dev](https://dictionaryapi.dev)

### 3.3 ElevenLabs Text-to-Speech (optional)

**Endpoint:** `https://api.elevenlabs.io/v1/text-to-speech/{voiceId}`

This service is **only used if you explicitly configure it** by entering your own ElevenLabs API key in the extension settings. When active, it sends:
- The text to be spoken
- Your ElevenLabs API key (as an HTTP header)

Your API key is stored in `chrome.storage.sync` and may be synced across your browser instances. It is never sent to DigiMob servers. ElevenLabs' privacy policy applies: [https://elevenlabs.io/privacy](https://elevenlabs.io/privacy)

If you use the default **Browser TTS** mode instead, all speech synthesis is handled entirely by your browser — no data is sent anywhere.

---

## 4. Browser Permissions

The extension requests the following permissions, which are required for its features to work:

| Permission | Why it is needed |
|------------|-----------------|
| `activeTab` | Access the content of the current tab to perform translations |
| `scripting` | Inject translation UI and overlays into web pages |
| `contextMenus` | Add "Translate" to the right-click context menu |
| `storage` | Store your settings, history, glossary, and bookmarks |
| `tabs` | Detect which tab is active and track translation state per tab |
| `<all_urls>` | Allow translation on any website you choose to use the extension on |

---

## 5. Children's Privacy

DigiTranslate does not knowingly collect data from anyone, including children under 13. As described above, the extension stores no personal data on any server.

---

## 6. Changes to This Policy

If the extension is updated in a way that changes data handling, this policy will be updated accordingly. The date at the top of this document reflects the last revision.

---

## 7. Contact

Questions about this privacy policy:

**Email:** support@digimob.app  
**Website:** [digimob.app](https://digimob.app)
