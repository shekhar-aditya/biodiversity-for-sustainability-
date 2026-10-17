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

Clicking an answer turns it green if it is right or red if it is wrong, and the correct answer is shown straight away.
The progress bar tracks the current loop. Answer options are shuffled too, so you learn the answer and not its position. You can turn this off.
Progress and any unfinished session are saved in the browser's localStorage.

Keyboard: `1`–`4` or `A`–`D` to answer, `Enter` for the next question.

## Editing questions

The bank is the `const questions = [...]` array in `index.html`:

```js
{ id: 1, week: "Week 0", question: "…", options: ["…", "…", "…", "…"], answer: 0 }
```

`answer` is the index of the correct option (0 = a). Week 12 answers were unofficial when the study pack was made.
Check them against the NPTEL solution once it is released.
