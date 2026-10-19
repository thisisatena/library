# Eti Library

A night-time reading room that recommends 3 spoiler-free books, reads each note aloud, and paints a cover for any book.

## Run
1. Unzip and open `index.html` in a browser (no build step, no server needed).
2. Click **API Settings**, paste your GapGPT API key and save. The key lives in tab memory only; it is never written to a file.
3. Pick your mood, age and language, then **Find My Three Books**.
4. Click a book to open it:
   - **Read this note aloud** uses `/audio/speech` (model `gpt-4o-mini-tts`, voice selectable).
   - **Paint this cover** uses `/images/generations` (model `gapgpt/qwen-image-2.1`, 1024x1024). The image also replaces the book's cover on the table.

## Files
- `index.html` structure
- `style.css` design and animation
- `app.js` API calls (chat, voice, image) and ambient effects

## Notes
- If you get a network or CORS error, the API does not allow direct browser calls. Put a tiny backend proxy in front of it.
- Never publish a page with a real key inside. Revoke any key that has been shared in public.
