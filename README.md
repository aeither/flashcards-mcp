# Flashcards by Fulin Labs

**Learn the words that matter in your daily life.**

Create personal vocabulary decks from your conversations, lessons, reading, work and travel. Study with examples, pronunciation and reversible cards in MCP Apps clients, or receive the complete deck as text and structured data in other clients.

- Website: https://flashcard.fulinlabs.com/
- Remote MCP: **https://flashcard.fulinlabs.com/api/mcp**
- Transport: Streamable HTTP (JSON responses); no account or API key required.
- Publisher: Giovanni Fu Lin, Fulin Labs — https://fulinlabs.com/
- Contact: giovannifulin@gmail.com
- Privacy: https://flashcard.fulinlabs.com/privacy
- Terms: https://flashcard.fulinlabs.com/terms

## Connect

Claude, Cursor, Grok and other remote MCP clients: add the remote MCP URL above. Choose HTTP / Streamable HTTP and no authentication. Adding a custom connection is separate from public directory approval.

```json
{
  "mcpServers": {
    "flashcards": {
      "url": "https://flashcard.fulinlabs.com/api/mcp"
    }
  }
}
```

Claude Code: `claude mcp add --transport http flashcards https://flashcard.fulinlabs.com/api/mcp`

Cursor: use the included `.mcp.json` configuration. The `.cursor-plugin` directory describes the marketplace package.

## Try it

- Make 10 Vietnamese flashcards for ordering my lunch, with English translations.
- Turn these words from my French lesson into flashcards: bonjour, merci, demain.
- Create 10 Japanese travel flashcards with kana readings and English translations.
- Save this deck on the website and give me a shareable study link.

## Tools and limits

`create_flashcard_deck` accepts a title and 1–100 complete cards. Each card has `front` and `back`, with optional pronunciation and translated examples. Supply `language` and `backLanguage` for language-learning decks. Chinese, Japanese and Vietnamese decks have additional example requirements described by the tool schema.

`create_website_deck` creates a persistent shareable link only when you ask to save or share. Anyone with that link can access the deck. It does not modify an existing deck or synchronize study history.

`speak_text` serves pronunciation for the study widget. Audio supports Chinese, English, French, German, Italian, Japanese, Korean, Spanish and Vietnamese. Other languages do not have supported audio.

The browser app provides spaced repetition and keeps study progress in local browser storage. Export a backup to preserve local data. This MCP does not read your browser library, review history, files, email or other connected accounts. Optional sharing and audio process the supplied content on servers. See the privacy policy for analytics and service providers.

This repository contains public connector metadata and installation instructions. It does not contain the hosted application source or private credentials. A package or registry entry does not imply endorsement by any AI platform.
