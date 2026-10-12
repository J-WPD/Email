# Inbox Companion prototype 0.1.1 downloads

[Download the complete prototype ZIP](https://github.com/J-WPD/Email/raw/refs/heads/codex/inbox-companion-downloads-20261012/Inbox-Companion-Prototype.zip)

The ZIP includes the Thunderbird add-on, both previews, the optional AI companion
source, and installation instructions. No credentials or private mailbox state
are included. These GitHub links are the delivery route; the original chat links
opened the cloud workspace viewer instead of downloading an attachment.

## Individual files

- [Thunderbird add-on](https://github.com/J-WPD/Email/raw/refs/heads/codex/inbox-companion-downloads-20261012/Inbox-Companion.xpi)
- [Thunderbird desktop preview](https://github.com/J-WPD/Email/raw/refs/heads/codex/inbox-companion-downloads-20261012/Thunderbird-preview.png)
- [Browser sample preview](https://github.com/J-WPD/Email/raw/refs/heads/codex/inbox-companion-downloads-20261012/Web-demo-preview.png)
- [Installation instructions](START-HERE.txt)
- [SHA-256 checksums](SHA256SUMS.txt)

If GitHub opens a ZIP/XPI file page, use its **Download raw file** arrow.
For a private repository, sign into GitHub with an account that has access.

## Install

Extract the ZIP. Keep the XPI as a single file. In Thunderbird 128 or later
(140 ESR recommended), open **Add-ons and Themes**, then select **Install Add-on
From File** from its gear/menu and choose `Inbox-Companion.xpi`.

The add-on uses your existing Thunderbird accounts. For AI, use Node.js
24 or later on the same computer. Open a terminal in the extracted `companion`
folder, run `npm ci` and `npm start`, and follow `START-HERE.txt` for pairing and
model configuration. Cloud-specific README paths should be replaced with your
own extracted companion folder.

OpenAI is now the default provider. Copy the source `.env.example` to `.env` and
set your own `APP_AI_KEY` securely there, using `AI_PROVIDER=openai` and
`AI_MODEL=gpt-4.1-mini`. Keep the key out of the add-on and version control; pair
the add-on with the separate local connection token. Selected email content is
sent to OpenAI only when you request an AI action. API billing is separate from
a ChatGPT subscription. Optional local Ollama remains available.

## Validation and limits

Native workspace reading, rules, local categories, native tag preservation,
account-matched reply drafts, archiving, and local companion pairing passed in
Thunderbird 140 ESR with synthetic Local Folders mail. All 36 automated tests
passed. The native and browser previews show synthetic/sample messages.

Actual AI inference and real-provider account sync remain unverified. Configure
your own OpenAI API key or optional local Ollama model before using AI features.
This is a Thunderbird add-on prototype, not a rebranded Thunderbird distribution.
No sending or permanent deletion is automated.

## Native preview

![Actual Thunderbird workspace with synthetic local mail](Thunderbird-preview.png)
