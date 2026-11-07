# Noor Majlis

A live Quran story and quiz game for a family or community gathering. One laptop runs the big screen, and everyone plays from their own phone.

**Play:** https://athermsyed.github.io/Noor-majlis/

## How an evening runs

1. **Join.** The host opens the link on the laptop connected to the TV and taps **Host on the big screen**. Players scan the QR code or open the link and type the 4-letter code. They enter a name, choose Brother or Sister, and add a photo if they want one.
2. **Welcome.** Shaykh Abdullah greets everyone with a recorded welcome.
3. **Story 1: The Ant Who Made an Excuse** (Surah An-Naml), told in five recorded parts while the scene changes behind him.
4. **Questions 1 to 10.** Each question appears on the big screen and on every phone with four large buttons and 22 seconds to answer.
5. **Top three**, then a **dua circle** around the winner. The dua is read aloud in English, and everyone taps Ameen on their phone.

Nobody is eliminated. Correct answers earn 100 points plus up to 50 for speed. After each question the correct answer stays on screen with its surah and ayah.

## Host admin

Open https://athermsyed.github.io/Noor-majlis/#admin (or tap **Host admin** on the start screen) and enter PIN **1111**.

- Edit any of the ten questions: the level, the question, the four answers, the correct answer, the reference and the note.
- Move questions up or down to change the order they are asked.
- **Save questions** saves them online, so the next game on any laptop uses them. No upload to GitHub is needed.
- **Reset to original** brings back the built-in questions (tap twice, then save).

## Player photo

After choosing a photo, the player drags it to move it and pinches or uses the slider to zoom, so the face fits inside the oval. **Adjust photo** reopens it, and **Remove photo** goes back to a drawn face.

## Design rules

- Prophets are never drawn. They appear only as a robed figure of light.
- Islamic phrases are shown as text and never spoken by the computer voice. Only "Bismillah", the questions and the English dua are spoken.
- Soft, long sounds only. No music.

## Technical notes

- A single self-contained `index.html`. The avatar art, the recorded narration and the game logic are all inside it.
- Live sync uses the Friday Arena Firebase Realtime Database under the path `fa/cc/nm/<code>`, and saved questions under `fa/cc/nm/admin/questions` (the section already open for Crowd Clash). If Firebase cannot be reached, it falls back to PeerJS.
- Hosted on GitHub Pages from the `main` branch.
