<!-- This file is published publicly (it is copied to the public repo kotobashi-releases when it changes). Do not put private information in it. -->

# Kotobashi

<p align="center"><img src="banner.png" alt="Kotobashi: a simple companion app for working across languages" width="640"></p>

<p align="center"><a href="https://github.com/riczescaran/kotobashi-releases/releases/latest">Download the latest release</a></p>

Kotobashi is a simple companion app for working across languages on your Mac. It translates, proofreads, and rewrites text in any app, translates whole documents and files, reads text from the screen, and follows conversations with live translated captions.

*About the name:* *kotoba* (言葉) means "words" and *hashi* (橋) means "bridge" in Japanese, so Kotobashi is a bridge for your words.

This repository only hosts the release downloads and the in-app update feed. The source code is kept private.

## Features

- **Translate and rewrite in any app.** Select text and press a shortcut (⌃⌥⌘T to translate, ⌃⌥⌘R to rewrite; both can be changed, and Settings warns you when a shortcut is already used by macOS or another app), click the small button that appears next to your selection, or right-click → Services.
- **Translate** detects the language for you. English goes to Japanese and everything else to English by default; you can change both languages and switch the direction.
- **Rewrite** text in its own language with a style: Proofread (fixes spelling, grammar, punctuation and clearly wrong words, and keeps your wording), Natural, Professional, Concise, Friendly, or your own styles.
- **Work with the result:** rewrites can highlight what changed (the eye button), *Check meaning* translates a translation back so you can see whether the meaning survived, *Replace* pastes the result over your selection, and line breaks and indentation are kept.
- **Translate whole documents and files** (new in 2.0): `.txt`, `.md`, `.rtf` and `.docx` files, saved next to the original. See [Translate files](#translate-files) below.
- **Translate from the screen** (⌃⌥⌘O): drag a box over an image, a video or a PDF, and Kotobashi reads the text on your Mac and translates it.
- **Live translated captions** (⌃⌥⌘L) for your microphone, one app (for example a Slack huddle) or both, in a floating bar, with a transcript you can copy or save. Speech recognition and translation run on your Mac.
- **Choose your AI:** your Claude or ChatGPT subscription (through the Claude Code or Codex command-line tools), an Anthropic, OpenAI or OpenRouter API key (OpenRouter gives you models from many providers with one key), or Apple's on-device translation and Apple Intelligence. If the chosen provider fails, Kotobashi can fall back to Apple's on-device options (on by default) and tells you why.
- **History** of your translations and rewrites, with search, favorites and CSV export.
- **Settings with search:** a sidebar like System Settings, and a search field that takes you straight to any setting.
- **Stays out of your way:** show it in the menu bar, the Dock, or both.

## Translate files

New in 2.0: Kotobashi translates a whole document, not only selected text.

- **Formats:** `.txt`, `.md`, `.rtf` and `.docx`. Anything else (a PDF, an image) shows "This file type isn't supported yet" and nothing runs.
- **Starting it:** menu bar → Translate ▸ **File…**, the shortcut ⌃⌥⌘F (it opens the Translate File window from any app, and you can change it in Settings → General → Shortcuts), dropping a file on the popup, or in Finder right-click a file → Services → *Translate File with Kotobashi*. You can also drop a file anywhere on the Translate File window.
- **Where it goes:** the translation is saved next to the original as `Name (Japanese).ext`, or in a folder you pick. The original is never changed and nothing is overwritten: if the name exists, the new file is `Name (Japanese) 2.ext`, then 3, and so on.
- **Long files:** they are translated in parts, one after another, with progress and a Stop button. Stop writes nothing. A part that fails is tried again and then translated with Apple's on-device translation, and the result tells you which parts.
- **What is kept:** text files keep every line break and indent. Markdown keeps its code blocks, inline code, link and image addresses, HTML and front matter exactly as they are. Word files are edited in place, so tables, images, lists, headings, styles and link addresses stay, and bold, italic, underline and links move to the matching words. RTF files keep fonts, lists, tables and links, but not images.
- **Not translated yet:** headers, footers and footnotes in Word files.
- **Good to know:** you can choose the AI provider for one file without changing your default. File translations are not saved to History. With an API key and a large file, Kotobashi tells you the cost before it starts.

## Install

1. Download the latest `Kotobashi-<version>.dmg` from [Releases](https://github.com/riczescaran/kotobashi-releases/releases/latest).
2. Open the `.dmg` and drag Kotobashi onto the Applications folder.
3. Open Kotobashi. The first time, macOS says "Apple could not verify Kotobashi is free of malware". Click **Done**.
4. Open System Settings → Privacy & Security, scroll down to the Kotobashi message, and click **Open Anyway**. Confirm with your password.

Requires macOS 26 or later.

## Updates

From the version that includes the updater onward, Kotobashi checks for new versions itself and installs them in the app (menu bar → Check for Updates…). Updates installed this way don't need the "Open Anyway" step again.
