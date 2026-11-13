# Chinese Study Notebook — Reader App
Created by Aye Chan

**You** make lessons in the Claude notebook (upload photo → generate).
**Everyone else** uses this app to study them. No upload, no AI, no API key needed.

The link between them is the file **lessons.json** in your GitHub repo.

---

## First time setup (repo: chinese-study)
Upload these 7 files to the repo (Add file → Upload files → Commit).
Replace the old files if they are already there:

    index.html  lessons.json  manifest.json  sw.js
    icon-192.png  icon-512.png  icon-maskable-512.png

Open https://charxil.github.io/chinese-study/ and install it (Android: ⬇ Install app; iPhone: Share → Add to Home Screen).

## Every time you add or change lessons in Claude
1. In the Claude notebook, tap **📋 Copy all data (JSON)** (left side, under the lessons).
2. On GitHub open the repo → click **lessons.json** → click the ✏️ pencil (Edit).
3. Select everything in the editor (Ctrl+A / long-press → Select all) → delete → **paste**.
4. Click **Commit changes…** → **Commit changes**.
5. Done. Users get the new lessons the next time they open the app (or ⚙️ Settings → Check for new lessons).
   You do NOT need to change sw.js for lesson updates.

Tip: if the paste looks empty or broken, press Copy in the notebook again and re-paste.
Lesson photos are not copied (to keep the file small); the app shows a 学 icon instead.

## What users can do in the app
- Study all lessons: 汉字, pinyin, English, မြန်မာ meaning, မြန်မာ sound, character breakdown, example sentences
- Flashcards, 汉字-only mode, hide/reveal, 🔊 audio, typed copy (📋 Copy)
- ✕ hides a word they already know — only on their own phone; ⚙️ Settings → Show all hidden words again
- Works offline with the last lessons it downloaded

## If you change index.html later
Upload the new index.html and in sw.js change `cs-viewer-v2` → `cs-viewer-v3` so phones update.
