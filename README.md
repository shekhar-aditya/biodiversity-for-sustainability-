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

## Answer key words

Nothing is highlighted while you are answering. After you answer, the correct option's key words are highlighted.
These are up to 4 words that appear nowhere in the question or in any other option, so they are what makes the answer the answer.
The same words are highlighted in the "Answer C: …" line and in the "Read these once before the loop" review list.
With this on, the automatic jump after a correct answer waits a little longer (1.2 s) so you can read them. It can be turned off in settings.

Clicking an answer turns it green if it is right or red if it is wrong, and the correct answer is shown straight away.
The progress bar tracks the current loop. Answer options are shuffled too, so you learn the answer and not its position. You can turn this off.
Progress and any unfinished session are saved in the browser's localStorage.

Keyboard: `1`–`4` or `A`–`D` to answer, `Enter` for the next question, `P` to pause or resume.

## Editing questions

The bank is the `const questions = [...]` array in `index.html`:

```js
{ id: 1, week: "Week 0", question: "…", options: ["…", "…", "…", "…"], answer: 0 }
```

`answer` is the index of the correct option (0 = a). Week 12 answers were unofficial when the study pack was made.
Check them against the NPTEL solution once it is released.
