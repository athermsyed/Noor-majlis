# Noor Majlis

A live Quran story and quiz game for a family or community gathering. One laptop runs the big screen, and everyone plays from their own phone.

**Play:** https://athermsyed.github.io/Noor-majlis/

## How an evening runs

1. **Join.** The host opens the link on the laptop connected to the TV and taps **Host on the big screen**. Players scan the QR code or open the link and type the 4-letter code. They enter a name, choose Brother or Sister, and add a photo if they want one.
2. **Welcome.** Shaykh Abdullah greets everyone with a recorded welcome.
3. **Story 1: The Ant Who Made an Excuse** (Surah An-Naml), told in five recorded parts while the scene changes behind him.
4. **Questions 1 to 7.** Each question appears on the big screen and on every phone with four large buttons and 20 seconds.
5. **Story 2: A Dua Under a Tree** (Surah Al-Qasas), told in five recorded parts as a break.
6. **Questions 8 to 10.**
7. **Top three**, then a **dua circle** around the winner. Everyone taps Ameen on their phone.

Nobody is eliminated. Correct answers earn 100 points plus up to 50 for speed. After each question the correct answer stays on screen with its surah and ayah.

## Design rules

- Prophets are never drawn. They appear only as a robed figure of light.
- Islamic phrases are shown as text and never spoken by the computer voice. Only "Bismillah" is spoken.
- Soft, long sounds only. No music.

## Technical notes

- A single self-contained `index.html`. The avatar art, the recorded narration and the game logic are all inside it.
- Live sync uses the Friday Arena Firebase Realtime Database under the path `fa/cc/nm/<code>` (the section already open for Crowd Clash). If Firebase cannot be reached, it falls back to PeerJS.
- Hosted on GitHub Pages from the `main` branch.
