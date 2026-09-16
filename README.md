# Lecture 8 – In-Class Pair Programming: Array and Object Methods

**Format:** Work with your partner. Take turns typing (switch "driver" every couple of parts).
**Time:** ~20 minutes. **Submit:** whatever you have at the end of class — finishing every part is not required.

Your `practice.js` already contains the data: a `numbers` array, a `students` array, and a `quizScores` object. Each part below asks a **question about that data**. Your job is to answer it using the right method from lecture.

**One rule: no `for` loops.** Every task below can be done in a single line with one method and a callback. That's the whole point of these methods — you describe *what* you want, not *how* to loop.

---

## Setup

1. **Open this project in VS Code.** Everything happens in `practice.js`.
2. **Run your code** with `node practice.js` in the terminal, or the **▷ Run** button / **F5**.

---

## Part 1 — forEach

Print each student's name on its own line.

## Part 2 — map

- Make a new array of just the students' **grades**.
- Make a new array where every grade is curved **up by 5 points**.

> 🤔 **Check:** after the curve, print `students[0].grade`. Is it the original number or the curved one? What does that tell you about `map`?

## Part 3 — filter and find

- Get all students with a grade **above 80**.
- Get the **first** student whose major is `'CSE'`.

> 🤔 **Discuss:** you just used two methods that both search. What's different about what each one *returns*? (Try `find` with a major nobody has, like `'BIO'`, and see what comes back.)

## Part 4 — reduce

Calculate the **total** of all student grades. Then use that to print the **class average**.

## Part 5 — every and some

- Did **every** student pass (grade of 60 or higher)?
- Did **any** student score above 90?

Each of these should print `true` or `false`.

## Part 6 — sort

- Sort the `students` so the **highest grade comes first**, then print just their names in that order.
- Now sort the `numbers` array using `.sort()` with **no callback**, and print it.

> 🤔 **Look closely at that second one.** `[12, 5, 8, 130, 44]` does not come out in the order you'd expect. Figure out what rule JavaScript used instead — then fix it by giving `.sort()` a callback so the numbers come out smallest to largest.

## Part 7 — Object.keys and Object.values

Using the `quizScores` object:

- Print an array of just the quiz names.
- Print an array of just the scores.
- **Then combine two methods:** calculate the total of all the quiz scores. (Hint: one method turns the object into an array, and you already used a method in Part 4 that adds up an array.)

---

## Bonus (if you finish early)

- **Chaining:** in a **single line**, get the names of all students with a grade above 80. (Two methods, one after the other — no intermediate variable.)
- **Reusable callback:** write a named function `isHighScore(student)` that returns true when the grade is above 80. Now pass that same function by name into both `.filter()` and `.some()`. Why is this nicer than writing the condition twice?
- **Count by group:** use `reduce` to build an **object** that counts how many students are in each major, like `{ CSE: 2, IE: 1, MATH: 1 }`. (Your accumulator starts as `{}` instead of `0`.)

---

## Wrap-Up

- Add a comment with both partners' names at the top of `practice.js`.
- Make sure the file runs top to bottom without errors.
- **Submit:** commit and push `practice.js` to your pair's repo before the end of class.

