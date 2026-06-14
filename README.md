# SignaVoice v3 🤟

A browser tool that reads your hand gestures through the webcam and speaks them out loud. No installation, no backend, no account — just open the HTML file and show your hand.

---

## What it does

You hold up a hand gesture in front of your camera. The app figures out what sign it is and says it out loud using your browser's built-in speech. That's basically it.

It knows 50+ gestures right now — things like thumbs up, peace sign, I love you (ASL), Namaste, directional signs, numbers, and a bunch of others. Full list below.

---

## Try it

👉 [Live demo](#) — hosted on GitHub Pages  
*(Allow camera access when prompted)*

---

## Gestures it knows

| Category | What's included |
|---|---|
| Greetings | Wave 👋, Peace ✌️, High Five 🖐️ |
| ASL | I Love You 🤟, L-shape, Pinky, Vulcan 🖖 |
| Numbers | Three 3️⃣, Four 4️⃣ |
| Directions | Up 👆, Down 👇, Left 👈, Right 👉 |
| Approval | Thumbs Up 👍, Thumbs Down 👎, OK 👌 |
| Commands | Stop ✋, Excuse Me ☝️, You 🫵 |
| Actions | Fist ✊, Punch 👊 |
| Expressions | Rock On 🤘, Snap 🫰, Pinch 🤏 |
| Cultural | Namaste 🙏, Heart Hands 🫶 |
| Misc | Call Me 🤙, Palm Up 🫴, Palm Down 🫳 |

---

## How it works under the hood

MediaPipe Hands (Google's library) tracks 21 points on your hand, 60 times a second. My code then looks at things like which fingers are extended, how far apart certain points are, and which direction the palm is facing — and matches that to a gesture in the dictionary.

No machine learning training involved. Just geometry.  ---

## Tech used

- **MediaPipe Hands** — hand tracking
- **Web Speech API** — the voice part
- **Vanilla JS** — all the gesture logic
- **HTML5 Canvas** — drawing the skeleton overlay on the video
- **CSS** — the UI (went a bit overboard with the hologram aesthetic)

---

## Running it yourself

Just open `SignaVoice-v3.html` in Chrome or Edge. That's it.

For the live demo via GitHub Pages:
1. Fork this repo
2. Go to Settings → Pages → set source to main branch
3. Open `https://yourusername.github.io/signavoice/SignaVoice-v3.html`

> Needs HTTPS for camera access to work. GitHub Pages handles that automatically.

---

## Privacy

Everything runs locally. Your camera feed never leaves your device — MediaPipe processes it on-device, and there's no server involved at all.

---

## Things you can tweak

- **Detection speed** — how many frames a gesture has to hold before it fires
- **Voice rate and pitch** — adjust how the speech sounds
- **Skeleton overlay** — toggle the hand landmark lines on/off

---
---

Made by Gaurav Jha  
