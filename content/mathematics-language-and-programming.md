---
title: "Mathematics, Language, and Programming"
date: 2024-11-21T19:33:27+01:00
draft: true
---

I haven't been writing a lot recently, but I read a couple of
[EWDs](https://www.cs.utexas.edu/~EWD/) out of frustration. I'm seriously
thinking about reading either _A Discipline of Programming_ by Dijkstra himself,
or _The Science of Programming_ by David Gries, which is accompanied by a
Foreword written by Dijkstra. When I read something written by Dijkstra, I
always agree with him—as far as I understand the subject he's writing about.

One quote of his always comes to my mind when programmers complain about
the relative importance of languages in the school curriculum… and about math,
of course:

> Besides a mathematical inclination, an exceptionally good mastery of one's
> native tongue is the most vital asset of a competent programmer.

I am a very poor mathematician, but unlike many other programmers, I am _not_
proud of it. I have a mathematical inclination, but a very limited knowledge.
But I see that mathematics can help us tremendously in software development,
even if it's just the simplest math. A couple of examples:

1. I cringed when Kent Beck wrote about _"All of the tricky code for rounding to
   three decimal digits […]"_ in the introduction to _Test Driven Development:
   By Example_. The code is not tricky, but requires simple arithmetic. If you'd
   like to round a money amount `x` to 0.01, just multiply it by 1/0.01, round
   it, and divide it by 1/1.01 again: `round(x*(1.0/0.01))/(1.0/0.01)`. It's
   a literal one-liner. What bothers me is not the word _tricky_, because this
   one-liner is an arithmetic trick, but the word _"all"_, which certainly
   is indicative of a significant amount of code having been written to solve
   this rounding issue.
2. I worked for a company that presented summarized textual content,
   interspersed with quotes from the original text. Layouts used to be done
   manually, with quotes in the margins. For the web version, especially for the
   mobile application, the quotes had to be displayed in between paragraphs. I
   figured out that this was quite easy by calculating the paragraph-quotes
   ratio, and then counting up a variable while displaying the text, adding that
   ratio to it. Whenever the variable surpassed another integer, a quote was due
   for display. Again: only addition, division, and rounding was required.
3. For a customer, I had to figure out how to perform a proper holiday
   computation, which is a bit tricky when the workload of an employee changes
   during the year, especially when holidays were already taken in that year. I
   walked away from the computer, used a whiteboard and later pen and paper to
   figure out a formula to compute the amount of holidays left. I also figured
   out that this formula can be simplified, eliminating a couple of parameters a
   function to compute those holidays left would require, reducing the amount of
   data that needs to be loaded from the database, and thereby improving
   performance. Once more: addition, subtraction, multiplication, division, and
   a few simplifications on high-school math level solved the problem.

What's most remarkable about this mathematical solutions is not that they are
complicated in any way, but that nobody working on that codebase came up with
those solutions, even though they have been considerably annoyed by the issues
for some time.

So having a mathematical inclination can be a far cry from being mathematically
proficient. Somebody who is mathematically inclined just will consider a
mathematical solution to a programming a possibility that has to be investigated
before resorting to trial-error programming. In that sense, I am mathematically
inclined.

English is not my native tongue, and I'm well aware of my limitations. This text
probably contains a couple of mistakes, both gramatically and orthographically,
and its style certainly could be improved by any high-school English teacher.

German is my native tongue, but even there a good high-school German teacher
will be able to point out mistakes in my writing. However, I am probably more
proficient in writing German than 95% or even 99% of the overall population,
because I read at least a dozen books written in German per year, and I also
write almost every day. Therefore, I also tick the second of Dijkstra's boxes:
_an exceptionally good mastery of one's native tongue_. Maybe I'm just the
one-eyed man in the country of the blind, but one is compared to his peers,
after all.

So I have the most vital assets of a competent programmer, now I just have to
_become_ that kind of programmer Dijkstra would consider competent.
