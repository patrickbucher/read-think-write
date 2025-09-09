---
title: "Procrastination Reveals Conflict"
date: 2025-02-09T09:42:25+01:00
---

I'm re-reading Neil A. Fiore's _The Now Habit_ to once again tackle my issue
with procrastination, which is still my biggest struggle concerning my
professional life. While few would describe me as a chronic procrastinator—I
handed in my Bachelor's thesis one week early, and I even file my taxes on
time—there are some important things I do procrastinate. My internal process is
usually messier than the output I produce, and only I know the struggle
involved for achieving the usual good results.

Having read _The Now Habit_ before, I struggled to implement the protocols
described therein. I had a hunch that one major issue, which probably not
applies to most readers, isn't discussed in the book: _unresolved_ or even
_undetected_ conflict.

What I like about the book is that it avoids Freudian psychoanalysis; i.e.
questions like _"What is wrong with me?"_ that only lead to more rumination
instead of productive action. However, one needs to detect possible underlying
causes to find proper countermeasures. In my case, the underlying issue is
_conflict avoidance_. 

I won't analyze the origins of this issue here, but I suspect that introverts
tend to be more conflict avoidant than extroverts, because arguing things out
with other people drains the introvert's social battery, while just analyzing
the conflict doesn't. (However, the avoidant behaviour of analyzing instead of
arguing provides the introvert with good arguments for dealing with the
conflict later. This could become useful, but only if the conflict is
revisited.)

One strong indicator for my hunch is that I hardly procrastinate in some areas
of my life, while I procrastinate a lot in others. Writing papers or finishing
school projects was never an issue, and neither is working on my personal
projects. Programming within an organisation, however, is sometimes a huge
issue. And as I reflect on the last 20 years, of which I spent most of the time
as a software developer in different companies, I can clearly see the
correlation between unresolved conflicts at the workplace and procrastination.

I love to program, but oftentimes I cannot get started. Once I think about a
task, all possible kinds of issues and eventualities start to unfold. This is
not bad per se, because my mind jumps on analyzing the task on autopilot, which
does neither require discipline nor willpower. Even avoiding the task for some
time can be productive, for my subconscious keeps dealing with it once I
internalized the problem to be solved. However, with all those stumbling blocks
I'm becoming aware of, I can't start writing code in a carefree manner. I'm too
worried about all kinds of possible issues.

One issue I frequently have is not of a technical but of a social nature: Even
though I have a solution in my mind that makes sense to me, I already
anticipate the reaction of the other programmers working on the same code base.
I had a lot of annoying discussions following the pattern _"Why did you do X
and not Y?"_. Those discussions sometimes revolve around technical issues, but
usually just around personal preferences. While the former discussions are
productive and facilitate learning, the latter ones are just annoying.

Those kinds of discussions are rarely conducted using reasonable arguments and
counterarguments. Instead, appeal to—absent and anonymous—authority is used, as
well as vague statements along the lines of _"nobody is doing it this way
nowadays"_ or, even worse, by yelling _"Clean Code!"_.

(Aside: The term _Clean Code_ is just as manipulative as _Agile Software
Development_. Just look for synonyms and antonyms for the adjectives "clean"
and "agile". You cannot argue against "clean" and "agile". Nobody wants "dirty"
code or "sluggish" software development.)

Let me illustrate the issue with an example.

### Enterprisey Startup Prototype

I recently got in touch with a former co-worker, who founded a company together
with some of his current co-workers. My business partner and I agreed to help
them working on a platform they're building. The goal is to figure out whether
or not we'd like to work together in the future. We invest little time, but if
both the collaboration and the platform look promising, we might get serious
about our collaboration. Until then, we'll only invest a couple of hours per
week, which aren't compensated financially.

In the first quarter of this year, the plan is to collaborate on a mobile
application, which is required to seriously tackle the market. I agreed to work
on the backend. The app is supposed to be a rough but working prototype. Since
time to market is crucial, the app is only a prototype, and the collaboration
doesn't come with any obligations, the usual reasons for
procrastinations—perfectionism, fear of failure or success—do not apply.

However, after the first hacking session, I found myself procrastinating on the
project for multiple weeks. I first thought that I was still too busy for most
of January. I finally found an hour to work on the project yesterday. I
accomplished very little—and procrastinated my efforts once more. But I also
started thinking about the development process so far.

During the first hacking session, I wrote very rough backend code for a REST
API: basic CRUD operations against a NoSQL database. Since I was writing a
prototype, I wrote the most straightforward code I could; everything in the
controller function, that is. However, my former co-worker insisted on
separating the service code from the controller code. Being one step away from
the clichéd three layer architecture, we refactored the code, which is now full
of single-line functions that just hand their parameters over to the next lower
layer: filling in forms instead of solving problems, as if we were writing Java
code.

We didn't argue that day, as we just wanted to go ahead and implement the CRUD
operations for the most crucial entities. And nobody had strong opinions
against splitting controller from service code, because we all did that before,
and it certainly isn't wrong. However, it was rather pointless, and there was
no good reason for the additional indirection at that stage of a prototype.

The next week, my former co-worker announced some changes to the prototype. He
_"challenged the code using ChatGPT"_, as he said, and applied the suggested
changes to the code base. I shrugged it off, because I just wanted to figure
out what my next tasks were supposed to be, and I'm mostly indifferent about
architecture discussions during the prototyping phase: it's all temporary
anyway, and it can always be changed. (However, I have a bias for the simplest
possible code structure when prototyping.)

So we put a list of tasks together, but I didn't work on any of those until
yesterday. And I didn't finish a single task, even though I had an empty
schedule yesterday in the afternoon. My motivation was completely gone. It felt
like a job now, just that I wasn't going to be paid for it. So why bother? I
played the drums and listened to a podcast instead.

It was only this morning that I realized what was going on: My former co-worker
argued using appeals to an _anonymous and absent authority_. Of course _one_
has to separate the controller code from the service code, that's how _it_ is
done. _Everybody_ does it like that. And there's no arguing against ChatGPT—the
Single Source of Unquestionable Truth. However, it would be interesting to know
whether or not the word "prototype" was part of the prompt that was supposed to
_"challenge the code"_.

Not only was the code dragged towards an enterprisey direction, one tiny
refactoring at a time, but also did the technical decisions reflect the power
structures of the organisation rather than the synthesis of a discussion among
peers. Also, time wasn't spent on finishing the prototype, but rather on
refactoring it while exercising power over the other developers.

My pragmatic decision of not pushing back (or rather: indecision) seemed
reasonable at the time. The goal was to finish a prototype quickly, i.e.
without wasting time on supposedly silly arguments. However, when I look at the
bigger context—figuring out if this collaboration is fruitful for both
parties—we'd better argued it out. Quitting my job to work for myself comes
with financial downsides. So at least I want to have the upside of working on
my own terms, or at least on terms that are acceptable for me. Working on
enterprisey code within an according power structure I can as well do somewhere
else, but _with_ decent financial compensation.

Therefore, I should absolutely argue such issues out in the future. Such
conflicts are unavoidable, and can even be productive! The question is, _how_
those conflicts are carried out. Are we arguing as peers and are we capable of
compromising in a way that works for both sides, or is one party required to
concede all the time because the other party exercises power using appeals to
anonymous and absent authority or based on "owning" the project?

Will carrying out this conflict have an effect on my procrastination within
said project? If so, the resolution of this yet _unresolved_ but no longer
_undetected_ conflict will show.
