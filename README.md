# LinkedIn Clean Feed

A Chrome/Brave extension that removes ads, promoted posts, suggestions, and clutter from your LinkedIn feed.

## What it blocks

- **Promoted posts** in your feed (multi-language support)
- **Suggested posts** and follow recommendations
- **Sidebar ads** and banner containers
- **Premium upsells** and "Try Premium" prompts
- **Promoted messages** in your inbox and messaging overlay
- **LinkedIn Learning** promos in the feed
- **"People You May Know"** suggestions
- **"Advertise"** links in navigation

## Install

### From Chrome Web Store
*Coming soon*

### Manual (developer mode)
1. Clone this repo
2. Open `chrome://extensions/` (or `brave://extensions/`)
3. Enable "Developer mode"
4. Click "Load unpacked" and select the project folder

## How it works

Two-layer approach for instant, flicker-free blocking:

1. **CSS rules** (`content.css`) — Injected at `document_start` before the page renders. Hides elements with stable CSS selectors (sidebar ads, premium upsells, etc.)
2. **Content script** (`content.js`) — Uses a MutationObserver to detect dynamically loaded content like promoted posts (identified by locale-matched text labels) and messaging spam.

## Privacy

This extension:
- Does **not** collect, store, or transmit any personal data
- Does **not** use analytics or tracking
- Only stores your on/off preference locally via `chrome.storage`
- Requires no permissions beyond `storage` and access to `linkedin.com`

## License

MIT
