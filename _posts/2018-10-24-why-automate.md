---
layout: post
title: Do we really need network automation?
---

TODO: reword this
Working everyday on the same you can become biased and so did I: this is why,
when speaking to someone new, I always assume that they believe in network
automation as much as I do. But people can be very surprising sometimes. :-)

In my mind, especially after seeing how automation massively helped one of the
largest global networks (Cloudflare - my current employer), I simply cannot
conceive that a network can run reliably without a form of automation. Yet there
still are plenty of examples of network running (often with major outages)
without anything at all. And they are happy with that, and reluctant to start
adopting automation methodologies.

In today's post I would like to share my views on some of the most frequent
"arguments" / claims (you name it) against automation. With this, my only goal
is to shed some light and bust some myths.

What is automation actually?
============================

One of the laws of thought states that, in order to ensure that we're speaking
the same language is to define the terms. I have searched for several
definitions for _automation_, and here's what I found:

- _"The technique, method, or system of operating or controlling a process by highly
automatic means, as by electronic devices, reducing human intervention to a
minimum."_
- _"The technique of making an apparatus, a process, or a system operate
automatically."_, where _automatically_ means _"Having a self-acting or
self-regulating mechanism"_.

On the other hand instead, automation is often (mis)understood as _just_
configuration management. Needless to say that configuration management is
indeed a major factor, but _definitely_ not the end goal. The most
important is what's the most painful to you and the one that's most boring for
the engineers in your team.

In simpler words: consider to automate whatever is the most painful to you, or
causing the most issues to your organisation. Start automating what you hate
doing the most. These are easy wins that will equally bring excitement in your
team seeing that automation actually works, but also creates more time for you
to automate more. The goal is, of course, to automate everything possible, but
it's always good to see early results.

What does "everything possible" mean? We now have so many sources of data
that give enough information about our networks, so the question is: what do you
do with all this data? The answer is not "Watch a monitor and when an event
occurs you run a command to deploy a configuration change": not only that this
conflicts with the definitions I shared above, but this process also would rely
on you to see the event at the right time and act on it before your customers
are impacted; sometimes, this might be too late. (Surely, assuming the
configuration change you apply manually is correct and it won't impact
negatively your network). In my opinion, you should aim for a self-healing
system that when it detects an event also applies the necessary changes.

But there's so much more to it than auto-remediation: what about the boring
notifications you need to write manually (i.e., in case of BGP session flapping,
interface flapping, massive packet loss caused by your transit providers, etc.).
Similarly, not always the system will be capable to fix the issue by itself, but
it can create the notifications for humans to investigate the issues further,
for example by raising a ticket.

At RIPE77 I had a talk that might help you see what I mean: _Automatic alerting
and notifications_ presents some good examples (the list can be nearly
infinite) of network automation beyond configuration management triggered by
running a command manually, i.e., automatic BGP prefix limit update when the
neighbours breach the existing limits, automatic Jira tickets raised when the
BGP password is incorrect, automatic emails sent to transit providers on high
service degradation due to packet loss, etc. You can similarly implement and
automate all of these for a more reliable, stable, self-resilient network.
This is network automation about.

Everyone needs to learn to code
===============================

This is one of the weakest arguments I've heard. No, not everyone has to learn
to code. At most your toolset might change and might be exposed to new a
slightly new world. Eventually, instead of CLI command X, you might execute the
CLI command Y, and that's pretty much it -- but the effect of what the command
does is the key here: it goes without saying that there'll forever be a
requirement for engineers that have to deeply understand the effect from a
networking perspective. Even more, if we think that the new command Y does a lot
more then the previous command X. Providing access to someone that doesn't
fully understand the implications, may lead to disastrous results.

We inherit most of the methodologies from the system side. If you look into the
structure of the system administration teams, you'll find out that they are
usually divided (but not a hard split) into engineers that continuously
develop and the rest that are (fully) dedicated to operations. There is no
reason why people would assume that the existing network operations team would
migrate over night to fully development. A softer delimitation between
developers and operational engineers that actively collaborate in a continuous
feedback loop is the winning combination in my opinion. I am also saying this
out of the experience I had in the last two teams I worked with. Operational
engineers don't have to write code. If they want however, they must be
encouraged, their initiative is laudable, but this cannot and it will never be
enforced.

To sum this up: I don't think it's feasible to assume that wiring code will ever
be a hard requirement. I do expect however small changes in the day to day
operations, but these are completely normal. Besides, network engineers are
smart and have always been able to adapt and learn new technologies. At the same
time, I would always encourage everyone to dive into writing code - at least for
fun. Kirk Byers periodically runs a nice Python course for beginners which I 
would recommend.

We'll loose our jobs
====================

No, we won't. Nobody will. In fact, all the companies that embraced automation
struggle to hire: there aren't as many candidates as open roles.

This excuse is somewhat related to the previous myth regarding the requirement
of writing code. Many people fear that automation would restrict everyone to
having to learn and write code, therefore they would be replaced. Well, I hope
that with the thoughts I shared previously, I've been able to clarify that this
scenario is surely impossible.

In fact that's not even the point. When I have attended APRICOT 2017, I had the
chance to seeing Tim O'Reilly speaking live on this exact topic. His keynote
is luckily recorded and I totally recommend you to watch it. If you don't have
the time right now, don't skip it. At the very, least bookmark it for later. The
key takeaway of this speech is that you should see the power of automation as an
opportunity for more meaningful and exciting jobs. Along the history, there are
plenty of examples of how automation transformed the world. Did we run out of
jobs? On the contrary.

Another interesting outcome to remember is the mixture of the machine with the

Invest in people
================


