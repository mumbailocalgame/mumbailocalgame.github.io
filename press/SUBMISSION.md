# Game Lab submission: Mumbai Local Straphanger

## Fill in on the Game Lab website

| Field | Value |
|---|---|
| Entry ID | *from your registration confirmation email* |
| Team member email | sijojoseph7509@gmail.com |
| Project title | **Mumbai Local Straphanger** |
| Playable game | https://mumbailocalgame.github.io/ |
| Documentation (PDF) | https://mumbailocalgame.github.io/press/mumbai-local-straphanger-design-doc.pdf |
| Video (trailer, 45 s) | https://mumbailocalgame.github.io/press/mumbai-local-straphanger-trailer.mp4 |
| Press kit (all of the above on one page) | https://mumbailocalgame.github.io/press/ |

All links were checked again after the v1.3 update (11 Oct 2026) from a fresh browser with no sign-in: every one returns the file directly (HTTP 200), with no login or access request.

### Optional mirrors (if the judges prefer Google Drive / YouTube)
The rules list Google Docs/Slides/Drive for documents and YouTube/Drive for videos as examples ("you may use…"). The links above already meet the requirement. To add mirrors:
1. **PDF → Google Drive:** upload `mumbai-local-straphanger-design-doc.pdf`, then *Share → General access → Anyone with the link → Viewer*.
2. **Video → YouTube:** upload `mumbai-local-straphanger-trailer.mp4` and set visibility to **Unlisted** or **Public** (not Private). It's vertical 1080×1920, so YouTube may show it as a Short; that's fine.
3. Open both links in a private/incognito window before submitting.

## One-line description
A balance game for phones: it's peak hour on the Virar fast, and you hold one overhead strap while the train lurches from Churchgate to Virar. Touch the left or right half of the screen to lean.

## Short description (≈100 words)
Mumbai Local Straphanger is built around one moment every Mumbai commuter knows: the train jerks, your feet slide, and a single leather strap keeps you off a stranger's lap. Touch the left or right half of the screen to lean against the sway. At the edge, time slows and the crowd gasps; pull back and the game freezes for a beat while your neighbours cheer. That's a *clutch save*. At stations you lean toward a cutting chai, a newspaper or an empty seat. Send any ride to a friend on WhatsApp and race their ghost. Drawn in a Mario Miranda-inspired ink style, in English, Hindi and Marathi.

## How judges should play (on a phone)
1. Open https://mumbailocalgame.github.io/ and tap the yellow ▶ button.
2. A 10-second tutorial teaches the controls (or tap *Skip tutorial*).
3. Hold the left half to lean left and the right half to lean right. Keep the needle in the green, watch for the yellow warning before each jerk, and recover from the red zone for a CLUTCH SAVE.
On a computer: the ← → arrow keys (or A/D).

## Files in this folder
- `mumbai-local-straphanger-design-doc.pdf`: 15-page game design document (v1.3) (source: `doc/design-doc.html`)
- `mumbai-local-straphanger-trailer.mp4`: 45 s vertical trailer with soundtrack (built by `../tools/make_trailer.py`)
- `press/`: the press-kit page published at /press/

---

## What changed in v1.3.1 (latest)
- **Illustrated characters in the game:** the four commuters, the neighbours and the chaiwala are now drawn from the same Figma AI illustrations used in the shop, not simple canvas shapes.
- **Natural movement:** the body bends at the hips (legs lean less than the upper body), the arm hinges at the shoulder, and the strap keeps a fixed length while its clamp slides along the rail with spring and damping. The strap goes slack when the hand rises. Feet take small steps, hop and stumble on jerks.
- **Full-screen shop:** it opens edge to edge, so the character art is no longer cut off, with the card centred vertically.
- **Accessories removed:** they didn't sit convincingly on the illustrated characters, so the Style tab, accessory purchases and streak accessory rewards are gone. Old saves that wore one are reset to none.

### Bugs and glitches fixed in v1.3.1
| Bug | Fix |
|---|---|
| Floating pieces of the strap ring appeared near the hand (the arm was cut out of the art with a rectangle, catching parts of the ring) | The arm is now traced from the ring down through connected pixels, keeping the head out |
| Empty straps hung right beside the player | Removed when the illustrated characters are in use |
| The game asked for 7 images that don't exist (404 errors on every load) | Build metadata removed from `sprites.json`, and the loader skips it |
| In the full-screen shop, the floating sound button sat on top of **Done** | The sound button hides while any sheet is open |
| The shop sheet was half height and cut off characters' heads | Full screen |
| Seated pose rose instead of sitting down | Fixed |

**QA (v1.3.1):** a scripted run through home, shop, records, a full ride to game over, a clutch save, a challenge link round-trip, and Marathi gameplay at 390×844. No page errors and no failed requests.

## What changed in v1.3
- **The save lands harder:** 0.12 s freeze-frame, relief face, neighbours cheer with speech bubbles ("Bach gaya!"), crowd gasp at the edge, relieved sigh, voice lines via the phone's own Hindi/Marathi/English voice.
- **Best-save replay:** your best clutch save replays in slow motion on the game-over screen and can be shared as a video.
- **Lean to choose:** at each station, chai / newspaper / headphones / a seat appear left and right; lean toward one to take it. Door vs middle standing position (door = ×1.5 coins, windier).
- **Social:** "Challenge a friend" sends a WhatsApp link with the exact same seeded ride and a ghost of your lean. No server needed.
- **Return reasons:** Central and Harbour lines, festival weeks (marigold torans, akash kandils, ×1.2 coins), Daily ride streaks.
- **Art:** Mario Miranda-inspired ink style: outlines, hatching, caricature faces, a packed back row; commuters glare when you lean on them.
- **Shop & UI:** full-screen shop with illustrated character cards and stat bars, springy motion, count-ups, confetti, ticking departure board, tap sounds.
- **Tuning:** first-minute difficulty retuned from a novice-player simulation: the slowest quarter of first rides goes from 13 s to 19 s, and rides with a clutch save from 47% to about 65%. Easy mode added.
- **Playtesting:** an on-device recorder (Records → Playtest data) with one-tap copy, for testing with real players.

## What changed in this build

**Core of the game: the clutch save.** Everything below supports one moment: teetering at the edge and pulling back.
- **Telegraphed jerks:** 0.6 s before each jerk, a yellow edge glow, arrows and a rail-joint "tick" show which side the shove is coming from.
- **Danger zone:** past 36°, time slows to 68%, the camera pushes in 4%, and a heartbeat speeds up as you near 45°.
- **Clutch save + combo:** recovering from above 40° to under 25° is a save. Saves within 12 s chain (×2, ×3…), with coins × combo and a reward chord that rises a semitone each step. The game-over screen shows saves and your best combo.

**Interface redesign.** Apple-style patterns (large titles, slide-up sheets, iOS switches, tab bar, island-style alerts) with music-app components (dark home screen, round play button, shelf of commuter "covers", ranked track list). Station-board yellow is the only accent, and the LED departure board is the recurring motif. Game over draws the Western line up to where you fell.

**Fonts.** Google Sans (UI and in-game text, including Devanagari) and Google Sans Code (departure-board text), both SIL Open Font License, bundled in `www/fonts/` so the apps work offline.

## Bugs fixed during QA
| Bug | Fix |
|---|---|
| On real phones the home screen and the commuter shelf could not be scrolled by touch (the page-wide scroll guard blocked them) | The scroll guard now lets the home list, shelf and sheets scroll |
| Swiping up while your finger was on the commuter shelf didn't scroll the page (the shelf only allowed sideways panning) | The shelf now passes vertical swipes to the page |
| "Churchgate" label on the game-over route line was centred off the left edge | Pinned to the first station dot |
| The gauge could crowd the LEAN labels on narrow phones | Gauge radius reduced on narrow screens |
| The Pause button stayed visible while falling but did nothing | Hidden during the fall; it comes back on the next ride or a second chance |
| Old pop-up text ("WHOA!") overlapped "ARRE BAAP RE!" when you fell | Pop-ups clear when you fall |
| "BEST" in the in-game HUD stayed in English when playing in Hindi/Marathi | Translated |
| Design doc: phones on page 8 ran into the footer, and the list on page 10 overflowed | Layout tightened; all 12 pages fit |
| Trailer text came out extra-wide (wrong font axis), the first caption ran off the edge, and "VIRAR FAST"/"PF 3" overlapped | Correct font axes, captions auto-fit, spacing measured |
| Tutorial step 1 could never finish (holding a side the whole time tipped you over) | Steps count time spent holding the correct side |

**QA performed:** scripted taps and swipes on three phone sizes (375×667, 360×780, 430×932), covering home, scrolling, all four sheets, tutorial, play, pause/resume, falling, game over, "Ride again" and a full Hindi pass. No console errors, no elements overflowing the screen, and the game-over sheet fits on the smallest screen. Repeated against the live site.

**Known limitations (honest notes):** difficulty is tuned with simulated players; real playtests with the built-in recorder are the next step. Voice lines depend on the phone having a Hindi/Marathi voice installed. The global leaderboard needs an online database switched on. The Hindi and Marathi text needs a native-speaker review. Online leaderboards aren't built yet. The web version has no ads; rewarded ads exist only in the (unreleased) app builds, using Google test IDs.
