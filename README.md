# Biodiversity Recall

A single-file MCQ drill for the NPTEL course **Biodiversity for Sustainability (noc26_bt56)**.
It covers all 130 assignment questions, Week 0 to Week 12.

Open `index.html` in any browser. There is nothing to install.

## How it works

1. **Weekly rapid fire.** Pick a week. Its 10 questions are fully shuffled and asked one at a time.
2. **Nested error loop.** Every question you miss goes into a new, reshuffled loop that contains only those misses.
   The loop repeats (for example 10 → 4 → 2 → 1) until you get through one with zero mistakes. Then the week is marked mastered.
3. **Grand Test.** All 130 questions from every week, fully shuffled.
4. **Final error loop.** Misses from the Grand Test go through the same nested loop until nothing is left.

## Timer and slow-question drill

- Every question has a live timer, and the total time for the loop runs alongside it.
- **Grand Test countdown:** each question gets 30 seconds by default (10, 15 or 20 s, or off, in settings).
  The bar turns amber at half time and red in the last quarter.
- When time runs out, the question stays open and the clock counts the extra seconds (+5.1s). Nothing is answered for you.
  A right answer given late still shows green, but it is marked "right but over time" and is not counted as correct.
  It counts as a miss in the score and stats, and the question comes back in the error loop.
- Weekly mode has no limit. The clock counts up and turns amber after 10 seconds.
- **Pause:** the Pause button (or the `P` key) stops the clock and hides the question until you resume, so a break never counts against your time.
  The clock also stops on its own while the tab is hidden or the phone is locked.
- **Live India time:** the quiz screen shows the current time in India (IST, Asia/Kolkata), updated every second.
- Each loop summary and each finished module lists the time you spent on every question, slowest first.
- The home screen shows your **slowest questions** (the average of your last 3 attempts at each) and a button that drills the 20 slowest as their own module, with the same countdown and error loops.

## Key phrases: question → answer

Nothing is highlighted while you are answering. After you answer, two things are highlighted:
- the **cue words in the question**, the part that tells you what is being asked (for example "microclimate regulation"),
- the **phrase in the correct option** that answers it (for example "Reducing heat stress" … "shade").

This teaches the pairing: when the question says X, look for Y in the options. Both lists are hand-picked for all 130 questions.
They are stored in each question's `qkeys` (question) and `keys` (correct option) fields.
The same highlights appear in the look-back view and in the "Read these once before the loop" review list.
After a correct answer the app waits 3 seconds before jumping on. Highlighting can be turned off in settings.

## Looking back

If the automatic jump moves on before you have read the highlighted answer, tap **← Back** (or press `←`).
The previous question appears again, answered, with its key phrases highlighted and marked "not scored". You can step back up to 20 questions.
The current question's clock is frozen while you look back. **Back to current question** (or `→` / `Enter`) continues it from where it was. Nothing you do while looking back changes your score.

Clicking an answer turns it green if it is right or red if it is wrong, and the correct answer is shown straight away.
The progress bar tracks the current loop. Answer options are shuffled too, so you learn the answer and not its position. You can turn this off.
Progress and any unfinished session are saved in the browser's localStorage.

Keyboard: `1`–`4` or `A`–`D` to answer, `Enter` for the next question, `P` to pause or resume, `←` to look back.

## Editing questions

The bank is the `const questions = [...]` array in `index.html`:

```js
{ id: 1, week: "Week 0", question: "…", options: ["…", "…", "…", "…"], answer: 0, qkeys: ["…"], keys: ["…"] }
```

`answer` is the index of the correct option (0 = a). `qkeys` are exact phrases from the question and `keys` exact phrases from the correct option, highlighted after answering. Week 12 answers were unofficial when the study pack was made.
Check them against the NPTEL solution once it is released.
