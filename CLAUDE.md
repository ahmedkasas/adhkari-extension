# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository contents

This repository currently contains a single static file: `privacy-policy.html`. It was added in one commit ("Add files via upload") via the GitHub web UI — there is no extension source code, `manifest.json`, build tooling, package manager config, or test suite in this repo.

`privacy-policy.html` is the bilingual (Arabic/English) privacy policy page for the "Adhkari" (أذكاري) Chrome extension — a prayer-times/adhkar browser extension referenced by the page but not itself present here. This page is almost certainly hosted via GitHub Pages and linked from the Chrome Web Store listing, which requires a public privacy policy URL.

The page has no build step: it's plain HTML with inline `<style>`, RTL Arabic content first, followed by an English translation, and a contact mailto link (`ahmedkasssas@gmail.com`).

## Working in this repo

- There is nothing to build, lint, or test — changes are direct edits to `privacy-policy.html`.
- To preview: open the file directly in a browser (no server required).
- Keep the Arabic and English sections in sync — every section in this policy is duplicated in both languages, and edits to policy terms (data collected, third-party services used, storage behavior) must be mirrored in both halves.
- Update the "آخر تحديث" / "Last updated" date line near the top of each language section when making substantive policy changes.
- The named third-party services (`aladhan.com` for prayer times, `bigdatacloud.net` for reverse geocoding) and the `chrome.storage` local-storage claim reflect the actual extension's data flow; don't change these claims without confirming they still match the extension's real behavior, since this is a legal/compliance document, not just marketing copy.

## If extension source code is added later

If the actual Adhkari extension codebase (manifest, background/content scripts, popup UI, etc.) gets added to this repo in the future, this file should be updated to document its structure, build/dev commands, and architecture — the current version intentionally describes only what exists today.
