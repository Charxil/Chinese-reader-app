# Chinese Study Notebook — Reader App
**Created by Aye Chan**

App link: **https://charxil.github.io/Chinese-reader-app/**

Learn Chinese from ready-made lessons: 汉字 · pinyin · English · မြန်မာ meaning · မြန်မာ sound · character breakdown · example sentences · flashcards · audio.

---

## 1. What you need to install · ဘာတွေ ထည့်သွင်းရမလဲ

| What | Needed? | Android | iPhone |
|---|---|---|---|
| The app itself | ✅ Required | Chrome → open the link → **⬇ Install app** | Safari → open the link → **Share → Add to Home Screen** |
| Chinese voice (for 🔊) | ✅ Usually already on the phone | Built in (Google Speech Services) | Built in |
| Myanmar voice (for 🔊 မြန်မာ and Read all 中→မြန်မာ) | ⭐ Optional | Install **SM Myanmar TTS** (free) | Not available. Chinese audio still works |

Nothing else is needed: no account, no Claude, no API key.

---

## 2. Install the app on your phone · App ထည့်သွင်းနည်း

**Android (Chrome)**
1. Open **https://charxil.github.io/Chinese-reader-app/** in **Chrome**.
2. Tap **⬇ Install app** at the top, or the menu **⋮ → Install app / Add to Home screen**.
3. The red **学** icon appears on your home screen. Open the app from this icon.

**iPhone / iPad (Safari)**
1. Open the link in **Safari**.
2. Tap **Share ⬆️ → Add to Home Screen → Add**.

---

## 3. Myanmar voice (optional) · မြန်မာအသံ ထည့်နည်း

Phones do not come with a Burmese voice. Without one, the app reads **Chinese only**.

### Step A: Install SM Myanmar TTS (free, Android)
1. Open **Google Play Store** and search **SM Myanmar TTS** (by Sao Mai Center for the Blind).
2. Tap **Install**. The app has no screen of its own; it adds a voice to your phone.

### Step B: Check it is on your phone
Open the phone **Settings**, search **text-to-speech**, and open **Text-to-speech output**.

| Phone | Path if search does not work |
|---|---|
| **OPPO / Realme** | Settings → Additional settings → Accessibility → Text-to-speech output *(or Accessibility & convenience → Accessibility → Vision)* |
| **Samsung** | Settings → General management → Text-to-speech |
| **Xiaomi / Redmi** | Settings → Additional settings → Languages & input → Text-to-speech output |
| **Google Pixel / others** | Settings → System → Languages → Text-to-speech output |

- **SM Myanmar TTS** should appear in the engine list.
- Keep **Preferred engine = Google**, so the Chinese voice keeps working.

### Step C: Choose the voice inside the app
1. Open the app → **⚙️ Settings → 🔊 Voices · အသံ**.
2. Under **Myanmar voice · မြန်မာ**, choose **SM Myanmar TTS** (or a voice with *my / mya / Myanmar* in its name).
3. Tap **▶** to test. You should hear "မင်္ဂလာပါ…".
4. If you hear nothing, try **System Myanmar voice (my-MM)** and tap ▶ again.
5. Close Settings and tap **🔊 Read all (中→မြန်မာ)**.

### Other free Myanmar voice
- **eSpeak NG** (Play Store, free) also has Burmese, but it sounds more robotic than SM Myanmar TTS.
- iPhone: no installable Burmese voice is available.

---

## 4. Using the app · အသုံးပြုနည်း

- **🔄 Refresh · သင်ခန်းစာအသစ် စစ်ရန်**: check for new lessons
- **🔊** red button: hear the Chinese word
- **🔊 မြန်မာ**: hear the Myanmar meaning (needs a Myanmar voice)
- **🔊 Read all (中→မြန်မာ)**: Chinese, then Myanmar meaning, for every word. Tap **⏹ Stop** to stop.
- **🃏 Flashcards**: Chinese character on the front, tap to flip
- **汉字 only**: blurs pinyin and sound so you practise reading characters
- **Hide 汉字 / pinyin / meaning**: self-test; tap a blurred item to reveal it
- **✕** on a word: hide a word you already know (only on your phone). Use **↩ Undo**, **↩ Show hidden words**, or **⚙️ Settings → Show all hidden words again** to bring it back.
- Works **offline** with the last lessons downloaded.

---

## 5. For the teacher (Aye Chan): updating

### Add or change lessons
1. In the Claude notebook, tap **📋 Copy all data (JSON)**.
2. On GitHub open **lessons.json** → ✏️ Edit → select all → delete → paste.
3. **Commit changes** (e.g. `Add lesson: Body Parts`).
4. Users get the lessons when they reopen the app or tap 🔄 Refresh.

### Update the app itself
1. Upload the new **index.html** and **sw.js** (Add file → Upload files → Commit).
2. `sw.js` line 2 must have a new version, e.g. `cs-viewer-v6` → `cs-viewer-v7`.
3. Wait 1–10 minutes, then close and reopen the app (twice if needed).

### Files in this repo
| File | What it is | Change it when… |
|---|---|---|
| `index.html` | The app | New features |
| `sw.js` | Offline support and updates | Every time `index.html` changes (bump version) |
| `lessons.json` | All lessons | You add or edit lessons |
| `manifest.json`, `icon-*.png` | App name and icon | Rarely |
| `README.md` | This guide | Optional |
