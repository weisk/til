---
title: Doing is normally distributed, learning is log-normal
subtitle: My conspiracy theory on why software estimation is such garbage 
date: 2024-05-28
tags: 
- communication
- econ-flavored
- law-of-diminishing-returns
- productivity
- psych-flavored
- the-medium-is-the-message
- time-management
- software-management
- software-dev
---

There are few things I think about more than the essays on
[gwern.net](https://gwern.net/index),
and there are few with as satisfying a theoretical payout
to contemplate in my orb as
[his essay on "leaky pipelines"](https://gwern.net/note/pipeline),
aka log-normal distributions.

The skulk: Say you're working on a Laravel web app.
You're about 90% sure you know how to start the app. You're
80% sure you know how to handle the infra you'll need to
get it online. And you're 70% sure you know how to get your
first customer. What is your chance of successfully going
from zero to first customer? 0.9 * 0.8 * 0.7 = a little over
0.5. That's ... a lot less encouraging than any of the
previous numbers, if you buy my multi-step modelling.

Software estimation is such a mess in part because
it has trouble recognizing that, at least,
[just-in-time](https://www.johndcook.com/blog/2010/03/03/just-in-case-versus-just-in-time/)
learning is at least *non-normally distributed*.
Everything we know about traditional project management,
from Waterfall to Gantt charts to estimation practices,
are on some level based around the idea that each individual
step in the chain is bell-shaped: A process taking twice as
long as it normally does might be 2 standard deviations out,
aka in the bottom 2.5% of outcomes. But in a log-normal
distribution, processes taking two, three, or five times as
long are much more common, and this throws things into
disarray. Some things happen much faster than usual - but
doing one estimated week-long project in half the time,
and another estimated week-long project in twice the time,
still leaves you in the red for your time budget.

Needless to say, it is almost never the case that in
software development you know all or even most of the 
technical hurdles you will face in the processs of development.
An 
[efficient markets hypothesis](https://en.wikipedia.org/wiki/Efficient-market_hypothesis)
fanboy might say "If anyone already knew how to do it, it would
already be done by now". I'm not that optimistic, but
I do think this leaky-pipeline approach can shed light
on some more counterintuitive things about our industry.

Such as the relentless emphasis, not only on relevant experience,
but on *knowing your specific tooling* when you apply to a given
job. You and I might be hardcore enough computer geeks that we
can pick up any language and be productive in it within a few
weeks, but if that doesn't hold for the *median* software
developer, then employers really are justified in deciding that
e.g. they only want to hire Java devs with previous experience
in... Java. If there's a 20% chance it takes 1 month, 20% for
2 months, ... 20% for 5 months before your non-Java-background
Java dev has enough experience to finally start contributing
to the Java codebase, then yeah, it makes a lot of sense not
to want to gamble on that. Not only do you face the possibility
of paying a five- or six-figure sum for someone who's useless,
you have very little ability to estimate as an employer
yourself when they will become useful.

Now what's really interesting about this theory is that
it suggests that **business processes that are normally-distributed
are the exception, not the norm**, in a sense.
*Every* new process a person has to undertake will have at
least some phase which is dominated by learning. That's as
true of web dev as it is of learning to operate the drive-thru
at McDonald's. It takes a special kind of rigor to transform
that into an activity routine and repeatable enough that you
get a long tail of normally-distributed, profitable activity.
Again, this makes sense: I've been building Django and Hugo
websites and web apps for a few years now, and I've been using
Python much longer than that, and I sort of have an intuitive
sense by now for how long either of them would take me. 
That's not because I'm some genius savant - it's because I have
already flowed through the leaky pipeline enough times
to know how I like to approach most things. The instant I'm
in new territory, we're back to the leaky pipeline. 

It may be the case that academic,
[just-in-case](https://www.johndcook.com/blog/2010/03/03/just-in-case-versus-just-in-time/) 
learning is less this way, because
the actual things you need to learn is carefully plotted
ahead of time for you. This would explain the popularity of
tutorials online, as ways to tamp down on the worst-case
scenario where that thing you thought would take you a week
to do ends up taking you a year. That being said, I definitely
had some classes in college that unexpectedly took way less
time to me (wireless communication, DSP) and some that
unexpectedly took way more (Maxwellian electromagnetism).
