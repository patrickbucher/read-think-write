---
title: "Domain and Machine Requirements"
date: 2025-12-30T09:38:52+01:00
---

I'm reading (and thereby [summarizing](https://github.com/patrickbucher/books/blob/master/meyer-agile-good-hype-ugly.pdf)) Eric Meyer's book _Agile! The Good, the Hype, and the Ugly_. In chapter 3, page 36, Meyer states an important distinction between two kinds or requirements:

1. _Domain_ requirements, describing properties of a model of the real world the system will be operating in.
1. _Machine_ requirements, describing desired properties of the system the project wants to build.

Even though Meyer makes it clear that this distinction has been emphasized for many years by [Jackson](https://en.wikipedia.org/wiki/Michael_A._Jackson_(computer_scientist)) and others, I wasn't aware of it until now.

A domain requirement is a given; something the project cannot decide on. Those are hard business rules, regulations, laws, or properties of the physical world. Examples: Any transaction exceeding USD 10,000 must be approved by a supervisor; the VAT rate for cars is 8.1%; the data must be stored within the EU; the speed of light is 299,792,458 meters per second.

A machine requirement can be negotiated with stakeholders; something the project wants to achieve. Those can be arbitrary goals such as: The system must process any transaction within 0.1 seconds; the user interface shall work on both desktop computers and mobile phones; a supervisor must confirm the deletion of a customer entry; the data will be stored on-premise. (Those are often—but not necessarily!—_non-functional_ requirements.)

Proponents of agile methods argue that requirements are just design decisions in disguise. While this might be true for some machine requirements, it's certainly not the case for domain requirements, which have to be just _gathered_ rather than negotiated with stakeholders.

### A New Perspective On A Failed Project

A couple of years ago, I've been working on a project re-implementing a software that just had been re-implemented and rolled out a couple of months earlier. The software was just way too slow for productive use from the start. I haven't been involved with that particular incarnation, but I heard the following story from multiple people involved:

The customer wanted a document management system that stored its documents in Switzerland. The contractor wanted to implement it using cloud technology that wasn't available in Switzerland back then. A compromise was made: The database server was to be located in Switzerland, while the application server was to be located in Amsterdam—the closest available location for the cloud technology to be used.

Most customers were located in Switzerland. So any request hitting the database had to travel from Switzerland to Amsterdam, then from Amsterdam to Zurich and back to fetch the data, and again from Amsterdam back to Switzerland to the customer. A road trip from, say, Lucerne to Amsterdam is 821km. (The road is probably a good rough approximation, for internet cables are often laid out alongside traffic routes.) The trip to Zurich has roughly the same distance.

So the database-hitting request will travel roughly four times 821km, which is 3284km. The speed of light, which is the maximum speed data can travel at, is 1,080,000,000 kilometers per hour. Since velocity is defined as distance traveled divided by time passed, the latency for said request is `3284km` divided by `1,080,000,000km/h`, which is equal to `3.04e-6h` or roughly `11ms`.

No matter how well the software is implemented and on what hardware it runs: every request has an overhead of `11ms`. This does not sound like much, but user interactions often involve multiple requests, and some of them to be performed in sequence. However, good engineering can reduce those additional costs. But there's nothing one can do about those `11ms` to begin with.

Either nobody thought of the issue before or it was just dismissed as irrelevant. The software was built, the customer was billed, the users disappointed—and the solution soon abandoned for a re-implementation with database and application running on the same server, located close to the users.

### Domain or Machine?

Could this costly disaster have been prevented? Well, this is easy to claim afterwards. But making the distinction between _domain_ and _machine_ requirements would raise some interesting questions. Are the following requirements unnegotiable domain requirements or subject for discussion as mere project goals, i.e. machine requirements?

- The user data shall be stored in Switzerland.
- The cloud service X of company Y located in Z shall be used.

While the first requirement looks like a good candidate for a domain requirement (the law demands storage within the country's borders), it could also be a mere preference or selling point for the project. Maybe users will pay up for having their data stored within the confines of their own country. Maybe a considerable performance hit is even acceptable for them. We don't know at this point, but we could at least ask the stakeholders: Do we need to store the data in Switzerland, or is this just a preference; _domain or machine_?

The second requirement smells like a preference of the contractor to use some new fancy technology that looks good on the company's portfolio and on the CV of its developers. However, chances are that the company was founded and funded by said cloud provider, and the contractor is obliged to use its technologies. This is just speculation, but it points to an important issue. Is the technology a given or just a preference; _domain or machine_?

Maybe a compromise could have been reached, or maybe the project should have been abandoned right at that point, saving the customer millions.

The successor project to re-implement the software deemed to slow for productive use was done using agile methods. Requirements were gathered as user stories, which are not proper requirements, but just scenario-based examples of system use, which is another point Meyer criticizes in his book.

Good user stories are _negotiable_ (as "n" in [invest](https://agilealliance.org/glossary/invest/)), and they have been negotiated a lot. Having agreed on a solution, the implementation often had to be stopped or changed because said negotiation transgressed hard business rules that exist in some areas, e.g. in finance.

### Conclusion

No matter if you order a software from a contractor or implement it using an agile or traditional plan-based process: by all means distinguish between _domain_ requirements, which _are_ carved in stone, and _machine_ requirements, which you are free to negotiate with the stakeholders involved.

Don't fail to negotiate the negotiable; and don't negotiate what's not negotiable.
