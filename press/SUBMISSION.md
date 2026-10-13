# Game Lab submission: Mumbai Local Straphanger

A self-initiated project for a game design challenge, by Sijo Joseph.

## Fill in on the submission form

| Field | Value |
|---|---|
| Entry ID | *from your registration confirmation email* |
| Team member email | sijojoseph7509@gmail.com |
| Project title | **Mumbai Local Straphanger** |
| Playable game | https://mumbailocalgame.github.io/ |
| Documentation (PDF, 24 pages) | https://mumbailocalgame.github.io/press/mumbai-local-straphanger-design-doc.pdf |
| Video (trailer, 45 s) | https://mumbailocalgame.github.io/press/mumbai-local-straphanger-trailer.mp4 |
| Everything in one ZIP | https://mumbailocalgame.github.io/press/mumbai-local-straphanger-submission.zip |
| Press page (all of the above) | https://mumbailocalgame.github.io/press/ |

Every link opens directly with no sign-in or access request.

### Optional mirrors
If the judges prefer Google Drive or YouTube: upload the PDF to Drive and set *General access → Anyone with the link → Viewer*; upload the trailer to YouTube as **Unlisted** or **Public**. Open both in a private window before submitting.

## One-line description
A balance game for phones: it's peak hour on a Mumbai local, and one overhead strap is all that keeps you on your feet. Hold the left or right half of the screen to lean.

## Short description (about 100 words)
Mumbai Local Straphanger is built around one moment every Mumbai commuter knows: the train jerks, your feet slide, and a single strap keeps you off a stranger's lap. Hold the left or right half of the screen to lean against the sway. At the edge, time slows, your body glows red and the crowd gasps; pull back and the game freezes while your neighbours cheer. That's a *clutch save*. Lean toward a chai-wala or a newspaper at stations, race a friend's ghost on the same train, and climb weekly leaderboards. Drawn in a Mario Miranda-inspired ink style, and fully playable in English, Hindi and Marathi.

## How judges should play (on a phone)
1. Open https://mumbailocalgame.github.io/ in any phone browser.
2. The game goes straight into a 10-second tutorial ride (or tap *Skip tutorial*).
3. Press and **hold** the left half to lean left, the right half to lean right. Keep the needle in the green, watch for the arrows before each jerk, and pull back from the red for a clutch save.
4. To see the other languages: Settings → Language (English → हिंदी → मराठी), live, without a restart.

On a computer: the ← → arrow keys (or A/D), and E for the ability.

## Highlights
- **The core moment:** telegraphed jerks (a 0.6 s warning), slow motion and a heartbeat at the edge, a danger glow around the body, a freeze-frame clutch save, and a slow-motion replay you can share.
- **Three languages:** 340 strings, each written in English, Hindi and Marathi, including station boards, announcements spoken by the phone's own voice, share cards and the daily story captions.
- **Decisions in the world:** at stations a vendor's arm reaches in from each edge; lean toward the one you want.
- **Four commuters, four abilities:** Second wind, Anchor, Iron grip and Quick hands, each upgradeable.
- **Reasons to come back, introduced gently:** features open one at a time over the first rides: missions, abilities, a commuter pass, a weekly rival, story panels, postcards and stickers, a 7-day daily pass.
- **Social:** seeded challenge links with a ghost, rematches, a personal-best ghost, weekly / longest-ride / total-distance leaderboards and private friend groups.
- **Five real lines:** Western, Central, Harbour, Trans-Harbour and Metro Line 1, plus monsoon, festival and peak-hour events.
- **Access:** colour-blind safe gauge, one-thumb mode, larger text, reduced motion, assist mode, and a friendly break nudge after 20 minutes.

## Files in the ZIP
- `mumbai-local-straphanger-design-doc.pdf`: 24-page game design document
- `mumbai-local-straphanger-trailer.mp4`: 45 s vertical trailer (1080×1920) with sound
- `game/`: the complete playable game (serve the folder with any local web server, or play online)
- `leaderboard-setup.sql`: the database setup for the online leaderboards
- `SUBMISSION.md`: this sheet

## Testing
Scripted touch tests on phone-browser screen sizes (360×640 to 430×932): first launch through the tutorial, play, pause, falling, game over, every tab and every Progress item, the shop on short screens, and a Hindi pass. No errors, no blank screens, nothing clipped.

## Honest notes
- Difficulty was tuned with a simulated novice player; playtests with real commuters are the next step.
- The Hindi and Marathi text was written with machine help; a review sheet is ready for native speakers.
- Online leaderboards need the Supabase database switched on; until then the boards show a clearly marked preview.
- Voice lines depend on the phone having a Hindi or Marathi voice installed.
- Illustrations were generated with Figma AI and cut into a moving rig by the project's own script.
