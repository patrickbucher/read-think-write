---
title: "Edsger W. Dijkstra: A Counterpoint"
date: 2024-11-15T22:56:46+01:00
---

In the short documentary [Discipline in
Thought](https://www.youtube.com/watch?v=W-nsB_83wLA&t=237s), Edsger W. Dijkstra
compares two different composition styles:

> There are very different programming styles. I tend to see them as Mozart
> versus Beethoven. When Mozart started to write, the composition was finished.
> He wrote the maniscript in one go. In beautiful handwriting, too. Beethoven
> was a doubter and a struggler, who started writing before he finished the
> composition and then glued corrections onto the page. In one place he did this
> nine times. When they peeled them, the last version proved identical to the
> first one. That iterative method of programming is somehow a very Anglo-Saxon
> custom. British education is pervaded by it. People learn, when they write,
> not to try to get it right the first time. Just write what's on your mind and
> then rewrite repeatedly to get the product you want. That's partly why word
> processors are marketed so aggressively and partly why they have been so
> successful there. While it is one of the advantages of working with pen and
> paper that when  you start a sentence, you should have it ready.

The late Dijkstra wrote is papers using pen and paper. A quick glance into the
[EWD Archive](https://www.cs.utexas.edu/~EWD/index07xx.html) suggests that
Dijkstra switched from a type writer to his fountain pen (the _Montblanc
Meisterstück_) as his main writing device in the early 1980s.

For Dijkstra, the process of writing is about bringing a finished thought to the
page. He clearly is on the side of Mozart in this respect. Paul Graham seems to
be on the Beethoven side, as he suggests in [Putting Ideas into
Words](https://paulgraham.com/words.html):

> I'll often spend 2 weeks on an essay and reread drafts 50 times.

Or in [How to Write Usefully](https://paulgraham.com/useful.html):

> I've never tried to count how many times I proofread essays, but I'm sure
> there are sentences I've read 100 times before publishing them.

Paul Graham is an advocate for LISP and [bottom-up
programming](https://paulgraham.com/progbot.html). 

> How do you divide a program? The traditional approach is called top-down
> design: you say "the purpose of the program is to do these seven things, so I
> divide it into seven major subroutines. [...] Experienced Lisp programmers
> divide up their programs differently. As well as top-down design, they follow
> a principle which could be called bottom-up design—changing the language to
> suit the problem.

Dijkstra, on the other hand, developed an operating system for a computer that
wasn't even built yet. He had to get it right without receiving any feedback
derived from running a program on actual hardware. LISP programmers, in
contrast, use a REPL (read-evaluate-print loop) to get immediate feedback.

Having been born in 1930, Dijkstra received most of his education during and
after World War II. Back in those days, paper probably was rare and expensive.
So you had to use it wisely. Even though paper became cheap later on, Dijkstra's
writing and thinking style was shaped under the idea that you should get it
right once you put in on paper.

He supposedly designed his algorithm for finding the shortest paths between
nodes in a weighted graph (named after him as [Dijkstra's
algorithm](https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm)) during a
coffee break:

> One morning I was shopping in Amsterdam with my young fiancée, and tired, we
> sat down on the café terrace to drink a cup of coffee and I was just thinking
> about whether I could do this, and I then designed the algorithm for the
> shortest path. As I said, it was a twenty-minute invention.

Not having pen and paper available was not an issue to him, quite to the
contrary:

> One of the reasons that it is so nice was that I designed it without pencil
> and paper. I learned later that one of the advantages of designing without
> pencil and paper is that you are almost forced to avoid all avoidable
> complexities.

Dijkstra wrote and published the paper three years later. He also thought about
the _shortest path_ problem a long time before, but he didn't bother writing
about it until he solved the problem.

This stands in contrast to Paul Graham's publication style (again from 
[How to Write Usefully](https://paulgraham.com/useful.html)):

> When I proofread an essay, there are usually passages that stick out in an
> annoying way, sometimes because they're clumsily written, and sometimes
> because I'm not sure they're true. The annoyance starts out unconscious, but
> after the tenth reading or so I'm saying "Ugh, that part" each time I hit it.
> They become like briars that catch your sleeve as you walk past. Usually I
> won't publish an essay till they're all gone—till I can read through the
> whole thing without the feeling of anything catching.

This approach can be described as _debugging into correctness_, whereas Dijkstra
_proofed correctness_ prior to writing and programming.

Having grown up with cheap paper and computers, my habits are more on Graham's
(or Beethoven's) than on Dijkstra's (or Mozart's) side. It would be interesting
to figure out if the two composers approached writing music differently: Did
Beethoven work bottom-up by starting with a couple of nice tunes that he put
together to great symphonies? And did Mozart start with a grand idea from which
he worked down to the melodies?

Arguably, both Beethoven and Mozart—and both Graham and Dijkstra—created great
works and influenced their field of expertise. So there's no "right" or "wrong"
approach, at least not judging by the outcome. I like to listen to Mozart's and
Beethoven's music. And both Graham and Dijkstra wrote essays that I learned a
lot from.
