# AI Mantra Counter — Prototype 01

## What this prototype does
- Uses the browser SpeechRecognition API.
- Listens for the English-transcribed phrase "Om Namah Shivaya".
- Counts matching phrases in finalized speech-recognition results.
- Shows progress and plays a simple bell when the selected target is reached.

## Run on Android
1. Put `index.html` on an HTTPS host (for example, GitHub Pages).
2. Open the HTTPS page in an up-to-date Chrome browser on Android.
3. Allow microphone access.
4. Select 108 and tap **Start listening**.
5. Chant clearly with a small pause between repetitions during the first tests.
6. Compare the result with a physical mala and note every missed or extra count.

Opening the file directly from local storage may not allow microphone access. A secure HTTPS page is recommended.

## Important limitations
This is a proof of concept, not a reliable finished japa counter. Browser speech recognition may be online, may not work on every Android browser, and may merge repeated chants or misrecognize Sanskrit/mantra pronunciation. This first version counts phrase matches in finalized transcript chunks, so it can undercount or overcount. Do not rely on it as the sole count until it passes repeated tests against a mala.

## Next engineering milestone
Collect consented test samples of the user's own chanting, then compare:
- browser speech recognition,
- offline Vosk / Whisper-based transcription,
- audio segmentation + phrase matching,
- a custom audio classifier trained to identify one complete repetition.

A robust counter should count one completed audio segment once, reject background speech, and expose a manual correction control.
