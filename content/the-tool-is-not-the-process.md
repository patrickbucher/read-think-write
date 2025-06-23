---
title: "The Tool Won't Use Itself"
date: 2025-06-23T18:12:36+02:00
---

I recently ranted about the pairing phase of a pair programming assignment (see [#20](/#20) and [#21](/#21)). Now that the assignment has been graded, I'd like to share some insight.

The assignment is about creating payslips. It involves calculating social security deductions based on a gross salary and a couple of rules that are in place here in Switzerland, e.g.:

> Deductions for unemployment benefits and accident insurance are due for a yearly(!) salary of CHF 2500.- and above.

This exclamation mark was literally there in the assignment; remember that for later. The students were supposed to write unit tests for various cases, e.g.:

> a 16 year old apprentice with a _monthly_ salary of CHF 700.-

I stated three rules and three specific examples. Now guess what deduction amount the unit test for the case above expected: Roughly half of the pairs got it wrong and expected _zero_ deductions. The four-eyes principle, which is a main selling point for pair programming, failed gloriously.

Yes, it's true: You _will_ always have a calculator at hand. But if you can't do any mental arithmetic whatsoever, you won't even think of using that calculator located right under your fingertips (TypeScript _is_ a rather powerful calculator). And the assignment certainly doesn't tell you to use it.

When you are capable of mental arithmetic, you'll notice right away that 12 times 700 is more than 2500. When you aren't, you won't even get a hunch that some arithmetic might come in handy here.

But it gets even worse: Most of those students had or still have a monthly salary in that very range—and those exact deductions! But they wrote a unit test expecting them to have no deductions in their payslip. They either never looked at the payslip, or just forgot that school could have a relationship to the real world once in a while.

So what's the moral of the story? You might have powerful tools that create the impression of replacing an entire set of skills. However, a total lack of said skills will also make it impossible to judge when a particular tool shall be used.

The frustration of practicing a skill that _can_ be replaced with a tool is actually useful: You will remember under what circumstances you longed for that tool! And when you relive this experience, you'll pick that tool up.

This is called _pathemata mathemata_: learning through struggle. Remove the struggle, remove the learning.

