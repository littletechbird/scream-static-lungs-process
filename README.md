# SCREAM

A fan-made music video for [N U B](https://www.youtube.com/watch?v=Ou04s3jfxII)'s song **SCREAM** (official audio), credited on the channel as N U B / nubarchive, released under Creative Commons Attribution (CC BY).

**The song and its rights belong to N U B.** This project is an unofficial fan music video. It is not affiliated with the artist, not endorsed by the artist, and claims no rights to the song. Thank you to N U B for releasing the track under CC BY.

Original song (official audio): [https://www.youtube.com/watch?v=Ou04s3jfxII](https://www.youtube.com/watch?v=Ou04s3jfxII)

The production logs also refer to this project as Static Lungs. The song title used throughout is SCREAM.

## Make your own

This video was directed by a music-video bot built from the [Tempotage template](https://x.ai/bot/0MgEiSVzQaByzMurkhxSs). Anyone can start from the same template and make their own.

This write-up is a full, honest record of how the video was made: the timeline, the tools, the people and agents, the prompts we actually have, the generation counts, the 4K pass, the usage readings, and what we learned. Every number comes from a log, a progress file, or a usage report. Where a number was never recorded, this page says so instead of guessing. All times are Pacific Time (PT).

A later, separate lip-sync test for Rue is noted at the end, under [A side note: the Rue dialog test](#a-side-note-the-rue-dialog-test). It was not cut into this music video.

## Contents

- [Make your own](#make-your-own)
- [The finished piece](#the-finished-piece)
- [The story and the tone](#the-story-and-the-tone)
- [Timeline](#timeline)
- [Tools](#tools)
- [How a take was checked (LOOK)](#how-a-take-was-checked-look)
- [Agents and roles](#agents-and-roles)
- [Generation counts](#generation-counts)
- [4K stats](#4k-stats)
- [Prompts](#prompts)
- [Usage and tokens](#usage-and-tokens)
- [Lessons learned](#lessons-learned)
- [Privacy](#privacy)
- [A side note: the Rue dialog test](#a-side-note-the-rue-dialog-test)
- [Appendix A: shot plan v1](#appendix-a-shot-plan-v1)
- [Appendix B: the cut, 30 segments](#appendix-b-the-cut-30-segments)
- [Appendix C: sample LOOK notes](#appendix-c-sample-look-notes)

## The finished piece

| | |
|---|---|
| Final file | `SCREAM 4K.mp4`, in the folder `SCREAM mv/4K`, on the home PC used for the upscale (an RTX 5060 Ti) |
| Picture | H.264 High, 3840×2160 (16:9), 24 fps, 6,238 frames (259.917 s of picture) |
| Length | Container and audio 259.946 s (4:20), matching the review cut with the song. The song master used for planning was logged at 259.95 s. |
| Audio | N U B's song, AAC, copied over. The audio packet MD5 was identical to the review cut. A codec, sample rate, and bitrate for the 4K audio stream were not logged beyond that match. |
| Size | 1,353,396,082 bytes |
| SHA-256 | `c378afddd42acac847bcfc48d773ed393ac5be0fc61d15524516aed8b0ba9628` |
| Approved cut (720p, with song) | 1280×720, 259.946 s, SHA-256 `5acf1a39f3e9a2682d1d0395adad9e6fad33a646e6a2bf3c73a6f7435a3d9905` |
| Silent master (720p) | 259.958 s, SHA-256 `5d263fb3db6cdff8124690800e8f402a09146f78fe6b4756484db84bcddd5a2e` |

The picture was built silent first, then a separate copy had the song laid underneath for review. The creator posted the finished video on X. No agent posted or uploaded it anywhere public.

## The story and the tone

A woman who has swallowed every word her whole life finds her voice in a cracked old guitar, and the gray city of TV-headed people starts to hear her.

The art direction was painterly cyberpunk anime illustration, in the same rendering family as the ARTAPOELC homage: a rain-gray, slate-blue city of static and CRT glow, where Rue's mustard-yellow raincoat and the guitar's amber light are the only warm colors until the final chorus floods the city with sunrise color.

The emotional through-line, from the shot plan:

1. **Swallowed** (0:00–0:49): polite, compressed, holding her breath; small private eye-rolls she never lets out.
2. **Cracks** (0:49–1:13): tiny accidental rebellions that surprise her more than anyone; guilty half-smiles.
3. **Reluctant reach** (1:13–2:04): she wants the guitar but keeps pulling back; the old life squeezes harder.
4. **First sound** (2:04–2:42): startled by her own sound, then hungry for it; one listener notices.
5. **Defiant** (2:42–3:01): playful, steady, no permission asked.
6. **Quiet resolve** (3:01–3:24): calm, a little teary; she recognizes herself.
7. **Release and company** (3:24–4:20): ecstatic, then warm; she makes room for someone else.

**Rue** (lead): an adult woman, about 25. Glossy black chin-length bob with blunt bangs, gray-blue eyes, light freckles, one visible small silver hoop earring. Mustard-yellow hooded raincoat over a black turtleneck, dark jeans, scuffed black boots. A faint amber glow behind her sternum grows through the song. **The guitar** is a battered vintage acoustic with honey-amber wood, a long crack mended with a stripe of gold tape, and a black strap; never electric. **Littlebird**, the Listener, appears only from shot 19 on: a round sky-blue bird head with three small head feathers, tan eyebrows, dark round eyes, a small pale-gray closed beak, black headphones around his neck, a peach-orange puffy jacket, dark slate jeans, and black shoes. **Screen-heads** are faceless commuters in gray coats whose heads are small vintage CRT televisions showing gray static.

Method rules used on this video, and on the two that followed:

- One still per shot, approved before motion.
- One 10 s 720p Grok Imagine image-to-video take per approved still; reshoot only failures.
- Motion law: no stills used as footage, no Ken Burns moves, no freeze frames, no reverse.
- Mouths stay closed. There is no singing or talking in the music video itself. (A later lip-sync test, not used in this cut, is described below.)
- No on-screen text, logos, captions, or readable signs. No gore. No photorealism. Every human is an adult.

## Timeline

### Friday, November 13, late afternoon: paper and stills

- **5:40 PM.** Weekly usage read 34.4% before work began (Ultra plan; the weekly limit resets Monday, November 16 at 3:10 PM PT). The song master was already in place. Lyrics and a local faster-whisper timing pass were done. Shot plan v1 was written: 30 shots. The full table is in [Appendix A](#appendix-a-shot-plan-v1).
- Character refs were generated first (3 gens, all passed on the first try): a Rue portrait, a Rue full-body sheet, and a painterly Littlebird ref.
- Then exactly one 16:9 still per shot, with the refs attached. Five stills were regenerated after LOOK failures (shot 11 twice, then shots 17, 28, and 29). Two stills (17 and 24) had garbled sign letters blurred locally, with no new generation. The raw frames were kept.
- **5:47 PM.** The stills pass was complete: 30 stills and two contact sheets. Generations totaled 38 (3 refs + 30 shots + 5 regenerations). Usage read 35.3%. Motion waited on the creator's approval of the stills.

### Friday, November 13, evening: motion, the cut, and 4K

- Usage before motion: 35.8%. One 10 s 720p image-to-video take was generated per approved still, in parallel lanes of six. Two long slots (20, 28, and also 30) used 12 s takes. Reshoot only on failure, one reshoot each.
- After 24 clips, usage read 39.0%.
- Two first takes failed and were reshot: shot 20 (a stumble, an open-mouth laugh, and eye-color drift) and shot 28 (repeated crowd faces and an open-teeth grin). Shot 23 was not reshot; a second Rue appeared at about 7.5 s, so only 0–7.0 s of the first take was used.
- Video gens totaled 32 (30 first takes + 20 t2 + 28 t2). Usage after motion: 40.3%.
- The rough cut was solved in `timeline.py` / `timeline v1.json`: plan boundaries were kept, shifted at most 1.21 s (the 29/30 boundary). Mild slow-motion, up to 1.154×, was used where a slot was longer than its clip. Hard cuts only; no freeze, no reverse, no Ken Burns. `freezedetect` found no frozen spans.
- `SCREAM rough cut v1 silent.mp4` (259.958 s) and the private review copy with the song (259.946 s) were built with ffmpeg. A contact sheet every 2 s was LOOKed across the whole cut.
- The 4K pass ran on the home PC (an RTX 5060 Ti) with the same Real-ESRGAN pipeline used on the ARTAPOELC homage (`realesr-animevideov3` ×3, lanczos to 3840×2160, x264 slow CRF 16, 24 fps, audio stream-copied from the review cut). The output is `SCREAM 4K.mp4`, 6,238 frames, 259.946 s, hash as in the table above. A 4K contact sheet and two detail crops were saved. A start time, an end time, and a PSNR reading for this 4K pass were not logged.

## Tools

| Tool | What it did here |
|---|---|
| yt-dlp and a local faster-whisper pass | The song master and planning timestamps. Lyric text came from the YouTube description; whisper segments were treated as ±1 s anchors only. |
| **GenerateImage** (Grok Imagine stills) | The 3 character refs and 35 per-shot stills (30 keepers + 5 retakes), 16:9, with refs attached. Two stills were repaired locally with a blur, not a new gen. |
| **Grok Imagine (GenerateVideo)** | Image-to-video, usually 10 s, 1280×720, from an approved still. Shots 20, 28, and 30 used 12 s takes. 32 clips in total. |
| ffmpeg / ffprobe | Contact sheets, trimming and any mild stretch, the hard-cut rough cut, laying the song under the picture, the 4K encode, `freezedetect`, and stream probes. |
| Real-ESRGAN `realesr-animevideov3`, ×3, then x264 CRF 16 | The 4K upscale on the home RTX 5060 Ti: 1280×720 to 3840×2160. |
| PowerShell runner (`run 4K.ps1`) | The same resumable 4K pipeline used on the ARTAPOELC homage: extract, upscale, encode. |
| SHA-256 checks | Copies of stills, refs, and later the cut were hash-checked on the home PC. |

## How a take was checked (LOOK)

"LOOK" means a person-style visual check of the real frames before anything is called done. It was used at every stage.

**Per still:** each still was inspected before the next one was generated. Typical failures were story mistakes (spending a later payoff too early), open mouths, or a weak character beat. Garbled letters on signs were blurred locally rather than regenerated.

**Per motion take:** a 10-frame 1 fps contact sheet for the whole clip, plus zoomed crops when hands, mouths, or faces looked off. Each take got PASS, KEEP-PARTIAL, or FAIL. Typical failures were open mouths, identity or eye-color drift, a stumble, duplicate people, or a crowd of identical faces.

**Rough cut:** a contact sheet every 2 s across the whole cut; `freezedetect` (no frozen spans).

**4K:** ffprobe; audio packet MD5 identical to the review cut; a contact sheet and two detail crops. A written PSNR of the 4K against the 720p cut, and a frame-by-frame 4K LOOK note, were not logged for this video.

## Agents and roles

| Agent | Role |
|---|---|
| **littletechbird** (human, the creator) | Creative lead. Approved stills before motion, reviewed the cut and the 4K, and posted the finished video on X. |
| **Director** (Tempotage, the video bot) | Wrote the shot plan, generated and LOOK-checked the refs, stills, and motion takes, built the silent cut and the review copy with the song, and ran the 4K pass. |
| **Motion lanes** | Image-to-video generation in parallel lanes of six, one take per shot, reshoot only on failure. |
| **Compiler** | Compiled this public write-up from the production plan and progress logs. |

## Generation counts

| | Count |
|---|---|
| Shots in the plan and the cut | **30** |
| Character refs | **3** (all passed first try) |
| Per-shot stills | **35** gens (30 keepers + 5 retakes: shot 11 twice, then 17, 28, 29) |
| Local still fixes, no new gen | **2** (garbled letters blurred on shots 17 and 24) |
| Still gens total | **38** |
| Motion clips | **32** (30 first takes + 2 reshoots: 20 t2 and 28 t2) |
| Clip spec | 10 s (12 s on shots 20, 28, and 30), 1280×720, image-to-video |
| Cut | 30 segments, hard cuts, mild stretch up to 1.154× on slots longer than the clip |

The still count adds up: 3 + 30 + 5 = 38. The motion count adds up: 30 + 2 = 32. 6,238 frames at 24 fps are 259.917 s of picture; the container duration, 259.946 s, matches the review cut with the song.

## 4K stats

| | |
|---|---|
| Frames | 6,238 |
| Output | 3840×2160, 24 fps, H.264 High, x264 slow CRF 16 |
| Audio | Stream-copied from the review cut; packet MD5 identical |
| Size / hash | 1,353,396,082 bytes, SHA-256 `c378afddd42acac847bcfc48d773ed393ac5be0fc61d15524516aed8b0ba9628` |
| Wall-clock upscale and encode times | not logged |
| Temporary 4K frames left on disk | not logged for this video |

## Prompts

### Hero and character

The character lock in `plan.md` is the description the stills and motion prompts were built around. It is quoted in [The story and the tone](#the-story-and-the-tone) and again with the full shot plan in [Appendix A](#appendix-a-shot-plan-v1).

Rules on every prompt, from the plan:

- mouth always closed (no singing, no talking, no open-mouth scream);
- no text, logos, captions, or readable signs;
- no gore and no photorealism;
- Rue stays in the mustard-yellow coat (except the gray blazer layer in shot 15);
- the guitar is never electric;
- no extra fingers; guitar hands stay simple;
- every human is an adult.

**Honest gap:** the exact text sent to GenerateImage and to Grok Imagine for each still and clip was **not saved to a file**. What was saved is the shot plan, where each slot's "Picture / action" and "Character beat" columns were the source for that slot's prompts, plus the per-shot LOOK notes. The prompts below are those plan lines, not verbatim API strings.

### Representative prompts (action text from the shot plan)

- **Swallowed (shot 01, 0:00):** "Rue sits on the floor of a tiny gray apartment at night, ear and palm pressed to the wall." Beat: eyes closed, waiting for the wall to answer; a hopeful breath that sinks into a resigned little exhale. Used: `01 t1` (PASS).
- **Cracks (shot 09, 1:01, "I'm done disappearing in the crowd"):** "High angle crosswalk, a flood of gray screen-heads; she stops dead still and the crowd parts around the yellow coat." Beat: chin lifts, shoulders square, eyes up at camera. Used: `09 t1` (the TV-head crowd streams around her while she stands still; the camera rises).
- **First sound (shot 17, 2:04):** "Rain rooftop at night over the static city; her first strum sends an amber ring of light rippling through the fog." Beat: startled wide eyes at her own sound, hand frozen over the strings. The first still was rejected (neutral face, no startle). Used: still take 2, then `17 t1` (PASS).
- **Quiet resolve (shot 25, 3:12, "I... won't... break..."):** "Bathroom mirror again: the reflection is now her real self in the yellow coat." Beat: palm pressed to the glass meeting her reflection's palm, a tiny teary smile. The progress log called this the strongest still beat of the set. Used: `25 t1`.
- **Company (shot 30, 4:08):** "Both sit on the roof edge at sunrise, guitar and ukulele on laps, city glowing." Beat: Rue gives one last sideways glance to camera, small closed-mouth smile, then looks back out at the sun. Used: `30 t1` (12 s).

The full shot plan is [Appendix A](#appendix-a-shot-plan-v1). The 30-segment edit list is [Appendix B](#appendix-b-the-cut-30-segments).

## Usage and tokens

**Plan:** Grok Bot Ultra. The weekly usage limit is shared with the other apps on the plan, so it isn't only Grok Bot. The limit reset Monday, November 16 at 3:10 PM PT.

**Weekly usage readings on November 13, from `progress.md`:**

| Time (PT) | Weekly usage | Source |
|---|---|---|
| 5:40 PM | 34.4% | before stills (earliest reading found for this project) |
| 5:47 PM | 35.3% | after the stills pass (38 gens) |
| (before motion) | 35.8% | start of the motion wave |
| after 24 clips | 39.0% | mid-motion check |
| after motion | 40.3% | after all 32 video gens (final reading found for this project) |

**Attributable project usage:** 0.9 points for stills (34.4% to 35.3%) plus 4.5 points for motion (35.8% to 40.3%), which is **5.4 points** of the weekly Ultra limit. There is a 0.5-point gap between 35.3% and 35.8% that is not logged as this project.

The 4K pass itself was a local Real-ESRGAN job, so it should not have added generation usage. No usage reading was logged after the 4K pass.

**Estimate, labeled as an estimate:** 5.4 points over a finished runtime of 259.946 s (4.33 minutes) is about **1.25% of weekly usage per minute of finished 4K**. If the unattributed 0.5-point gap is included (5.9 points), the estimate is about **1.36% per minute**. These are estimates from the logged percentages and the runtime, not a metered per-clip cost.

This is the cleanest of the three stills-first videos: two motion reshoots, no later recut of the master. How that compares with the other two videos, and with the working claim of "about 1% per minute," is discussed with the summary table that accompanies these write-ups.

**Raw token counts are not available.** No log or report used here records input or output tokens, per-clip generation cost, or a dollar figure, so none is estimated here. On-demand or extra-credit use was not logged for this project.

## Lessons learned

1. **Approving one still per shot, then taking one motion pass, is a much cheaper method than a many-takes generation burn.** The earlier ARTAPOELC homage logged 57.2 weekly points during a 564-clip burn for a 4:47 video. This 30-shot video used 38 still gens and 32 motion gens, and 5.4 attributable weekly points, for a 4:20 master.
2. **Story mistakes show up in the still, if you look.** Shot 11's first two stills already had Rue playing the guitar, which would have spent the "first sound" payoff in shot 17. Those stills were rejected before any motion was spent. Shot 29's first still had both characters already seated and playing, which would have duplicated shot 30; it was also rejected at the still stage.
3. **Open mouths were the most common motion failure, even when the still was closed.** Shots 20 and 28 failed their first takes on open-mouth laughs (20 also stumbled and drifted eye color; 28 also repeated one face across the crowd). The second takes passed with closed smiles. Several other takes passed with a note to hold a clenched jaw or a still grin.
4. **A trim can save a reshoot.** Shot 23's first take grew a second Rue at about 7.5 s. Using only 0–7.0 s avoided a new generation.
5. **Readable letters still sneak onto signs.** Shots 17 and 24 were saved with a local blur rather than another still gen. The motion prompts also had to forbid indoor rain on shots 13 and 23, because rain streaks had been painted into those stills.
6. **A successful command is not visual success.** Every still and take was LOOKed. The 4K pass was hash-checked and had an identical audio packet MD5, plus a contact sheet and crops. A PSNR against the 720p cut was not logged here, unlike the ARTAPOELC homage; that is a gap, not a proof that the check was skipped or performed.
7. **Keep the silent master separate.** Building silent first, then laying the song under a separate copy, kept the music out of everything except the review copy.

## Privacy

Folder names and short file names are shown, but this write-up does not include full file paths from a personal PC, machine IDs, or email addresses. The upscale machine is described as the home PC (an RTX 5060 Ti) used for the 4K pass. The creator is named as littletechbird.

---

## A side note: the Rue dialog test

This test is **not in the music video**. It was a later, separate experiment (November 14) to see whether a short spoken line could be lip-synced to Rue without leaving the same painterly look.

The picked line was: "You can mute me. You can't turn me off." Other candidates were "I'm not static. I'm just tuning in." and "Sorry. I don't come in gray."

A new rooftop close-up still was generated with GenerateImage (Grok Imagine), using the Rue portrait and the shot-22 still as refs. It passed on the first try. Voice was a Higgsfield seed-audio preset (Ainsley). Video was Higgsfield Wan 2.7, 5 s, 720p, with the still as the start image and the padded spoken line as the audio reference. A 5 s Wan 2.7 clip was preflighted at 7.5 credits; the voice preflight was logged at 0.3 credits. After the test, the Higgsfield balance had fallen from 35.33 to 27.53 credits, a spend of 7.8 credits. One of three planned video attempts and one of two voice attempts were used; take 1 was kept as the final.

LOOK notes: the audio passed through unchanged (cross-correlation lag 0 ms, r = 0.9996). Bilabial closures landed on "mute" / "me", with a rounded "oo" on "mute", a wide "ee" on "me", an open shape on "can't", and lips closing after "off". Weak spots: the lips part about 250 ms before the first word, and the mouth stays half-open with teeth through the 0.4 s pause. Teeth stayed clean, with no jaw warp. Identity held (bob, bangs, freckles, coat); a second hoop appears on the far ear mid-clip. The style stayed painterly, not photoreal. It ends on a closed-mouth smirk.

The finished test is `rue dialog test.mp4`, 1280×720, 30 fps, 5.04 s, with AAC audio, SHA-256 starting `561365e6` and ending `ed7dc`. Weekly usage around the test was logged at 49.3% before and 49.9% after, with a note that the limit is shared and another job was running at the same time, so that 0.6-point change is not treated here as the cost of the test alone.

The creator's response, logged after review, was that the test was great. It remains a side experiment, not a shot in the SCREAM cut.

---

## Appendix A: shot plan v1

From `plan.md`, the 30-shot plan the video was cut to. The preamble below is lightly edited from the production file so that local paths and personal names are not copied here. The shot table itself is the plan's table.

Song: N U B, "SCREAM" (official audio), CC BY, [https://www.youtube.com/watch?v=Ou04s3jfxII](https://www.youtube.com/watch?v=Ou04s3jfxII). The song master was logged at 259.95 s (4:20). Timing: local faster-whisper (small) segments on the full mix, ±1 s, with lyric text from the YouTube description. Those times were planning anchors only.

**Thesis:** A woman who has swallowed every word her whole life finds her voice in a cracked old guitar, and the gray city of TV-headed people starts to hear her.

**Art direction:** Painterly cyberpunk anime illustration (same rendering family as ARTAPOELC), a rain-gray slate-blue city of static and CRT glow where Rue's mustard-yellow raincoat and the guitar's amber light are the only warm colors until the final chorus floods the city with sunrise color.

**Character lock and anti-list:** as in [The story and the tone](#the-story-and-the-tone).

**Generation plan (stills first):** refs first (3 gens), then exactly one 16:9 still per shot (30 gens) with the refs attached. Regenerate only on LOOK failure. Motion only after the stills were approved.

| # | Time | Lyric under it | Picture / action | Character beat | Arc |
|---|------|----------------|------------------|----------------|-----|
| 01 | 0:00-0:12 | "I wanna scream / I wanna shake the room / I wanna hear the walls answer back" | Rue sits on the floor of a tiny gray apartment at night, ear and palm pressed to the wall | Eyes closed, waiting for the wall to answer; a hopeful breath that sinks into a resigned little exhale | Swallowed |
| 02 | 0:12-0:24 | "Every headline sounds the same / ... somebody left to blame / Static filling up my lungs" | Packed subway car of screen-heads; gray static mist drifts toward her | Lowers her phone, slides her eyes left and right at the TV-heads, then presses a hand to her chest and holds her breath, cheeks tight | Swallowed |
| 03 | 0:24-0:30 | "Every mirror edits me / Every version feels like someone I don't wanna be" | Restroom mirror: her reflection wears a gray office blazer and a perfect polite smile | Rue tilts her head and narrows her eyes; the reflection keeps smiling | Swallowed |
| 04 | 0:30-0:36 | "Hands tied up in second guesses / Living off reactions, choking on impressions" | Office desk, her wrists loosely tangled in phone-charging cables, monitor full of glowing heart and thumbs icons | Gives the tangled cables a small tug, then a dry deadpan side-look to camera | Swallowed |
| 05 | 0:36-0:42 | "Don't say calm down / Don't say hold tight / I've been swallowing my words my whole life" | A screen-head boss pats her shoulder | Lips pressed tight, polite nod, while her fist clenches under the desk | Swallowed |
| 06 | 0:42-0:49 | "My mouth won't move / My pulse won't lie / Something's breaking underneath tonight" | Night rain street; amber glow pulses in her chest; hairline cracks of amber light spread in the wet pavement under her boots | Stops mid-step, looks down at the cracks, curious, fingers touching her sternum | Swallowed -> cracks |
| 07 | 0:49-0:55 | "I wanna scream till the silence gives / Break every version I was told to live" | Row of shop windows, each reflection a different gray "version" of her | Taps one window with a fingertip and it spiderweb-cracks; surprised half-smile at herself | Cracks |
| 08 | 0:55-1:01 | "Cut the signal / Kill the noise / Find the part of me they couldn't destroy" | Rain alley, she has just yanked the plug of a loud buzzing static-screen sign; the alley goes dark and quiet | Plug in hand, guilty-pleased glance over her shoulder | Cracks |
| 09 | 1:01-1:13 | "Pull me under / Pull me through ... / If nobody hears me I'll still be loud / I'm done disappearing in the crowd" | High angle crosswalk, a flood of gray screen-heads; she stops dead still and the crowd parts around the yellow coat | Chin lifts, shoulders square, eyes up at camera | Cracks |
| 10 | 1:13-1:24 | "I wanna scream / I wanna scream" | Dim pawn shop; the gold-taped guitar hangs on the wall, glowing faintly amber | Reaches toward it, pulls her hand back to her chest, glances at the price-less tag, reaches again | Reluctant reach |
| 11 | 1:24-1:34 | (break) / "Built from cracks they couldn't see / Held together by adrenaline and cheap belief" | Her apartment, sitting on the bed with the guitar across her lap | Traces the gold-taped crack with one fingertip; a small soft smile she doesn't let get too big | Reluctant reach |
| 12 | 1:34-1:40 | "Every promise lost its shape / Now I'm carrying the weight of every word I never say" | Climbing a stairwell with a huge sack of crumpled paper notes and blank speech bubbles on her back | Stops, sighs, hitches the sack higher, keeps climbing | Reluctant reach |
| 13 | 1:40-1:45 | "Running circles in my head / Fighting conversations that were never even said" | Small kitchen at night, pacing; faint ghost-outlines of arguments swirl around her head | Points sharply at an empty chair mid-argument, then catches herself, embarrassed, lowers the finger | Reluctant reach |
| 14 | 1:45-1:51 | "Every step feels automatic / Trying not to panic while I fake the habit" | Open-plan office, rows of screen-heads typing in unison | She is one beat out of sync, freezes, then forces a too-bright fake smile | Reluctant reach |
| 15 | 1:51-1:57 | "Don't call this peace / Don't call this home / I've been wearing someone else's skin too long" | Elevator; she shrugs off a stiff gray blazer revealing the yellow raincoat | Holds the blazer at arm's length, one eyebrow up like it smells, drops it | Reluctant reach |
| 16 | 1:57-2:04 | "The room gets small / The air gets thin / I'm done letting all this live within" | Apartment walls and ceiling squeezing in around her, guitar clutched to her | Arms braced against both walls, teeth set, then she pushes and the walls stop | Reluctant reach -> first sound |
| 17 | 2:04-2:10 | "I wanna scream till the silence gives / Break every version I was told to live" | Rain rooftop at night over the static city; her first strum sends an amber ring of light rippling through the fog | Startled wide eyes at her own sound, hand frozen over the strings | First sound |
| 18 | 2:10-2:21 | "Cut the signal / Kill the noise ... / Pull me under / Pull me through" | Same rooftop, billboards of static around her flicker out one by one; heavy rain | Grins (closed mouth), eyes closing, leans into a harder strum | First sound |
| 19 | 2:21-2:30 | "If nobody hears me I'll still be loud / I'm done disappearing in the crowd" | Street below, crowd of screen-heads; one figure among them is Littlebird, looking up | Littlebird pulls his headphones off his neck and stares up, amazed; on the roof edge Rue notices him and gives a tiny nod | First sound |
| 20 | 2:30-2:42 | "I wanna scream / I wanna scream" (+ instrumental) | Rue runs down a zigzag fire escape, guitar on her back | Jumps the last steps, glances back up at the roof with a breathless grin | First sound |
| 21 | 2:42-2:48 | "Turn it up / Turn it off / Every voice is just another mask" | Walking against a flow of screen-heads, she flicks a TV-head's screen as she passes and its static clears to a surprised human face (closed mouth) | Playful flick, smirk over her shoulder | Defiant |
| 22 | 2:48-2:54 | "Push me down / Watch me rise / You don't get to write my life" | Shoved down on the wet crosswalk, guitar case beside her | Rises from one knee, brushes rain off her sleeve, steady level stare up into camera | Defiant |
| 23 | 2:54-3:01 | "No more hiding / No more waiting / No more asking for permission" | Office: she slides her ID badge across the desk to the screen-head boss, guitar case on her shoulder | Polite little wave goodbye, eyebrows up, already turning to leave | Defiant |
| 24 | 3:01-3:12 | "I... won't... fade... / Not this time" | Empty subway platform, a train's light washing over her | Slow deep breath, hand on chest, amber glow steady and calm, eyes open and sure | Quiet resolve |
| 25 | 3:12-3:24 | "I... won't... break... / Not for you" | Bathroom mirror again: the reflection is now her real self in the yellow coat | Palm pressed to the glass meeting her reflection's palm, a tiny teary smile | Quiet resolve |
| 26 | 3:24-3:31 | "I wanna scream till the silence cracks / Leave every empty expectation in the past" | Rooftop at dawn, she strums and a giant amber shockwave cracks the gray sky like glass | Head tipped back, eyes shut, mouth closed, pure release | Release |
| 27 | 3:31-3:42 | "Burn the script / Erase the role / Take back every piece they stole / Pull me under ... / I remember who I answer to" | Golden shards of all her gray "versions" drift back to her | Catches one shard, presses it to her chest, then a knowing smile to camera | Release |
| 28 | 3:42-3:54 | "If nobody hears me I'll still be loud / You can't bury what won't back down" | Street below: the crowd's screens have cleared to real faces looking up; sunrise color floods the city | Rue lifts the guitar overhead, closed-mouth laugh, eyes squeezed happy | Release |
| 29 | 3:54-4:08 | "I wanna scream / I wanna scream" | Littlebird steps out of the rooftop door hugging a small ukulele | Rue, seated on the ledge, reaches an open welcoming hand to him; Littlebird peeks up shyly | Company |
| 30 | 4:08-4:20 | "I wanna scream" (outro) | Both sit on the roof edge at sunrise, guitar and ukulele on laps, city glowing | Rue gives one last sideways glance to camera, small closed-mouth smile, then looks back out at the sun | Company |

---

## Appendix B: the cut, 30 segments

From `timeline v1.json` and `build.sh`. 1280×720, 24 fps, silent first, hard cuts only. Each segment is taken from the start of its clip (`01 t1.mp4` through `30 t1.mp4`, except shots 20 and 28, which use t2). When a slot is longer than the source clip, the segment is time-stretched, up to 1.154× (shot 29). Shot 23 uses only the first 7.0 s of `23 t1` (a second Rue appears at about 7.5 s). Times are song time, in seconds.

| # | Song in | Song out | Dur | Clip | Stretch | Notes |
|---|---|---|---|---|---|---|
| 01 | 0.000 | 11.542 | 11.542 | 01 t1 | 1.149 | |
| 02 | 11.542 | 23.083 | 11.542 | 02 t1 | 1.149 | boundary shifted −0.46 s from the plan |
| 03 | 23.083 | 30.000 | 6.917 | 03 t1 | 1.000 | boundary shifted −0.92 s |
| 04 | 30.000 | 36.000 | 6.000 | 04 t1 | 1.000 | |
| 05 | 36.000 | 42.000 | 6.000 | 05 t1 | 1.000 | |
| 06 | 42.000 | 49.000 | 7.000 | 06 t1 | 1.000 | |
| 07 | 49.000 | 55.000 | 6.000 | 07 t1 | 1.000 | |
| 08 | 55.000 | 61.500 | 6.500 | 08 t1 | 1.000 | |
| 09 | 61.500 | 72.833 | 11.333 | 09 t1 | 1.129 | |
| 10 | 72.833 | 83.708 | 10.875 | 10 t1 | 1.083 | |
| 11 | 83.708 | 93.917 | 10.208 | 11 t1 | 1.017 | |
| 12 | 93.917 | 100.000 | 6.083 | 12 t1 | 1.000 | |
| 13 | 100.000 | 105.000 | 5.000 | 13 t1 | 1.000 | |
| 14 | 105.000 | 111.000 | 6.000 | 14 t1 | 1.000 | |
| 15 | 111.000 | 117.000 | 6.000 | 15 t1 | 1.000 | |
| 16 | 117.000 | 124.000 | 7.000 | 16 t1 | 1.000 | |
| 17 | 124.000 | 130.208 | 6.208 | 17 t1 | 1.000 | |
| 18 | 130.208 | 140.792 | 10.583 | 18 t1 | 1.054 | |
| 19 | 140.792 | 150.000 | 9.208 | 19 t1 | 1.000 | |
| 20 | 150.000 | 162.000 | 12.000 | 20 t2 | 1.000 | reshoot; 12 s source |
| 21 | 162.000 | 168.000 | 6.000 | 21 t1 | 1.000 | |
| 22 | 168.000 | 174.125 | 6.125 | 22 t1 | 1.000 | |
| 23 | 174.125 | 181.250 | 7.125 | 23 t1 | 1.018 | only 0–7.0 s of the take used |
| 24 | 181.250 | 192.167 | 10.917 | 24 t1 | 1.087 | |
| 25 | 192.167 | 203.500 | 11.333 | 25 t1 | 1.129 | |
| 26 | 203.500 | 211.292 | 7.792 | 26 t1 | 1.000 | |
| 27 | 211.292 | 222.042 | 10.750 | 27 t1 | 1.071 | |
| 28 | 222.042 | 235.208 | 13.167 | 28 t2 | 1.093 | reshoot; 12 s source |
| 29 | 235.208 | 246.792 | 11.583 | 29 t1 | 1.154 | largest stretch; largest boundary shift (+1.21 s) |
| 30 | 246.792 | 259.950 | 13.158 | 30 t1 | 1.093 | 12 s source; boundary shifted −1.21 s |

The silent file was logged at 259.958 s; the review copy with the song, which the 4K pass used, was logged at 259.946 s.

---

## Appendix C: sample LOOK notes

From `progress.md`. This is a sample of the stills and motion notes, not a substitute for the full log.

**Stills, rejected and then passed:**

- **11 take 1, rejected (story):** she is already fretting and strumming; that spends the first-sound payoff (shot 17). **Take 2, rejected (story):** still in a playing grip on her lap. **Take 3, PASS:** guitar lying on the bed, she rests her chin on her arm and touches the gold tape with one fingertip; soft held-back smile.
- **17 take 1, rejected (character beat):** neutral face, no startle; the light swirl reads as magic, not a sound ring. **Take 2, PASS** after a local blur of garbled letters on a billboard: wide startled eyes, hand lifted off the strings, amber rings from the soundhole.
- **28 take 1, rejected (mouth rule):** a wide open-mouth laugh reads as singing or screaming, and she is standing in the crowd instead of on the roof. **Take 2, PASS:** Rue alone on the roof edge with the guitar overhead, eyes shut, smiling, lips nearly closed, and the crowd's screens now show faces looking up.
- **29 take 1, rejected (character beat):** both already seated and playing, which duplicates 30. **Take 2, PASS:** Littlebird at the rooftop door hugging his ukulele; Rue, seated, reaches an open welcoming hand.

**Motion failures and trims:**

- **20 t1, FAIL:** stumble with hands in a puddle at 6–7 s, then an open-mouth laugh and eye-color drift from about 8 s. **20 t2 (12 s), PASS:** runs down the fire escape, lands, looks up smiling; lips slightly parted in the smile at 8–11 s, not talking or singing.
- **23 t1, PASS trimmed:** a second Rue with a lanyard appears at about 7.5 s, so only 0–7.0 s is used.
- **28 t1, FAIL:** every crowd face is the same young man; open-teeth grin at about 8.5 s. **28 t2 (12 s), PASS:** TV heads turn into varied adult faces from about 4 s (older woman, bearded man, woman with braids and glasses, gray-haired man); Rue's smile is closed.
