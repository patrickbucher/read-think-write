---
title: "Mathematics, Language, and Programming"
date: 2024-11-21T19:33:27+01:00
---

I haven't been writing a lot recently, but I read a couple of
[EWDs](https://www.cs.utexas.edu/~EWD/) out of frustration. I'm seriously
thinking about reading either _A Discipline of Programming_ by Dijkstra himself,
or _The Science of Programming_ by David Gries, which is accompanied by a
foreword written by Dijkstra. When I read something written by Dijkstra, I
always agree with him—as far as I understand the subject he's writing about.

One quote from [EWD
498](https://www.cs.utexas.edu/~EWD/transcriptions/EWD04xx/EWD498.html) always
comes to my mind when programmers complain about the relative importance of
languages in the school curriculum… and about math, of course:

> Besides a mathematical inclination, an exceptionally good mastery of one's
> native tongue is the most vital asset of a competent programmer.

I am a very poor mathematician, but unlike many other programmers, I am _not_
proud of it. I have a mathematical inclination, but a very limited knowledge.
However, I understand that mathematics can help us tremendously in software
development, even if it's just the simplest math. A couple of examples:

1. I cringed when Kent Beck wrote about _"All of the tricky code for rounding to
   three decimal digits […]"_ in the introduction to _Test Driven Development:
   By Example_. The code is not tricky, it just requires simple arithmetic. If
   you'd like to round a money amount `x` to, say, a granularity of 0.05, just
   multiply it by 1/0.05 (i.e. scaling it up), round it, and divide it by 1/0.05
   (i.e. scaling it down): `round(x*(1.0/0.05))/(1.0/0.05)`.  It's a literal
   one-liner. What bothers me is not the word _tricky_, because this one-liner
   can be considered an arithmetic trick, but the word _"all"_, which certainly
   is indicative of a significant amount of code having been written to solve
   this petty issue.
2. I worked for a company that presents summarized textual content interspersed
   with quotes from the original text. Layouts used to be done manually, with
   quotes in the margins. For the web version, especially for the mobile
   application, the quotes had to be displayed in between paragraphs. The
   simplest solution was to just tuck them in between the topmost paragraphs,
   until there were no quotes left, leaving the gaps between paragraphs empty
   further down below. I figured out an easy solution by calculating the
   paragraph-quotes ratio (one quote after every `n` paragraphs), and then
   counting up a floating point variable while displaying the paragraphs, adding
   that ratio to the counting variable after each gap. Whenever the variable
   surpassed another whole number, a quote was due for display. Again: only
   addition, division, and rounding was required.
3. For a time-tracking software, I had to figure out how to perform a proper
   holiday computation, which is a bit tricky when the workload of an employee
   changes during the year, especially when holidays were already taken in that
   year. I walked away from the computer, used a combination of the whiteboard
   and pen and paper to figure out a formula to compute the amount of holidays
   left. Thereby I realized that the formula could be simplified, eliminating a
   couple of parameters such a function would require, reducing the amount of
   data that needs to be loaded from the database, and thereby improving
   performance before writing a single line of code. Once more: addition,
   subtraction, multiplication, division, and a few simplifications on
   high-school math level solved the problem.

What's most remarkable about these mathematical solutions is not that they are
complicated in any way, but that nobody working on that codebase came up with
them, even though the underlying issues caused significant pain and weren't
resolved for quite some time.

So having a mathematical inclination can be a far cry from being mathematically
proficient. Somebody who is mathematically inclined just considers a
mathematical solution to a programming problem a possibility that has to be
investigated before resorting to trial-error programming done so often. In that
sense, I am rather mathematically inclined.

English is not my native tongue, and I'm well aware of my limitations. This text
probably contains a couple of mistakes, both gramatically and orthographically,
and its style certainly could be improved by any high-school English teacher.

German is my native tongue, but even there a good high-school German teacher
would be able to point out mistakes in my writing. However, I am probably more
proficient in writing German than 95% or even 99% of the general population,
because I read at least a dozen books written in German per year, and I also
write almost every day. Therefore, I also tick the second of Dijkstra's boxes:
_an exceptionally good mastery of one's native tongue_. Maybe I'm just the
one-eyed man in the country of the blind, but one is compared to his peers,
after all.

So I have the most vital assets of a competent programmer, now I just have to
_become_ that kind of programmer Dijkstra would consider competent. The question
is: how to become that competent programmer I'd like to be?

Tackling _The Science of Programming_ right away probably is a bad idea, because
it introduces both new mathematical techniques and its application to
programming problems. I'd rather learn about mathematical techniques before, and
just then tackle their applications to programming.

_Concrete Mathematics_ by Knuth et al. is certainly a good introduction for the
kind of mathematics needed in computer science. With its roughly 450 pages, it's
considerably longer than _The Science of Programming_. It featuers exercises on
six difficulty levels, of which I only consider doing the ones of the lower two
or three levels: I'd like to become a mathematically inclined, competent
programmer, not a mathematician, after all.

I always saw mathematics as an exercise in purification of the mind. It also
purifies solutions for everyday programming problems, which then require far
less testing than solutions built-up using the programming by trial and error
paradigm that is so prevalent nowadays.

I must not forget to read good texts in my native tongue alongside. However,
English is programming's native tongue, so reading good English texts certainly
is helpful, too. Morris Kline's _Mathematics in Western Culture_, which is also
recommended by Dijkstra in multiple EWDs, would certainly make for a good
accompanying read.
