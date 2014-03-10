---
layout: post
title: Release it - Notes. 
published: false
---

"Release It" by Michel Nigard has been forever in my to-read list, not until now I need it the most. With DevOps methodology rising, I ended up more involved
 with the support of a production system that I also help develop. In that moment the Book was a mandatory read for me.

## What they do not teach in school.

>Statistics gurantee that the majority of programmers have nerver worked on really large, mission-critical software.  First, salary surveys consistently show that most programmers have less than ten years of experience. Second the histogram of project sizes is heavely weighted toward the smaller end of te scale. So, take a young population with the relatively few opportunities to work on a giant projects, and it's not surprice that experience at that level is hard to find. 
>
>These issues certainly aren't covered in colleges and universitites. Where opotimization rergeres to tweaking up some search algorithm.


That alone is the main reason why I am happy I read the book. As mentioned several time in the book, getting your application to ship is only half the battle. Your application still has to survive in the field, with failing integration points, high peak  of concurrent users or slow responses from a third party web services. This book is packed with expirience and advices to make your application ready to survive __"production"__. 


## Miscomceptions tackle by the book

   1. You need accept the fact that despite your best laid plans, bad things will happen.
   2. Relize that "Release 1.0" is not the end of the development project but the begining of the system's life on its own.

### Patterns and Antipatterns for Production ready software

Antipatterns:

   * Slow Response
   * Blocked Threads
   * Integration Points - Number one killer of systems. without timeouts is a surefire way to create cascading failures or acelerate cracks in a system.
   * Chain Reactions
   * Cascading Failures
   * Unbalanced Capacities
   * Unbounded Resultsets
   * Atttacks of Self Denial

Patterns:

   * Bulkheads. Damage contaiment. Like in ships, bulkheads prevents water from moving from one section to another avoiding the ship to sink.
   * Decoupling middleware. Avoid many failures modes throught total decoupling. Learn many architectures and chose among them, Not every asystem needs to look like a three-tier application with an Orable Database, Learn many architectural styles and select the best architecture for the problme at hand.
   * Circuit Braker
   * Use Timeouts
   * Fail Fast 
   * Handshaking


## Quotes

Some great quotes I gather from the book:

>Design and architecture decisions are also financial decisions. These choices must be made with and eye toward their implementation cost as well as their downstream costs

----

>In the world of bussines it all come down to money. Systems cost money. And to stay in bussines, you need to make money.

----

>Why Agile? Their emphasis on early delivery and incremental improvements means software gets into production quickly. Since production is the only place to learn how the software will repond to real-world stimuli. I avocate any appproach that begins the learning process as soon as possible.

----

>Enterprise Software systems - enterprise class symple means that the software must be availbale , or the company loses money.

----

>Bugs will happen. They cannot be eliminated, so they must be survived insted."

----

>I relaized that the devlment team weer building everthing to pass testing, not to run in production."

----

>The true birth of a system comes not on the day that design and development begins, or even when the project is conceived, but on the day it launches into production. This is a beginning, not an end. Over time, the system will grow and mature. It will gain new features. It will lose defects, and perhaps gain some too. It will become what it was meant to be, or, even better, it will become what it needs to be. Most of all, it must change. As system that cannot adapt to its environment is stillborn.

----

>The funsion of thecnical and financial viewpoints is one of the most imporatnt recurring themes in this book.



## NOTES TO CLEANUP


"The ariline was moving toward a service-oriented architecture... most large companies have some cariation of this project under way now"

Examples as problems with slow response making all threads waiting :S Timeouts...

The worst problem here is that the bug in one system could propagate to all other affected systems. Inside every enterpirse today is a mesh of interconnected, interdependent system. They cannot - must not - allow bugs to cause a chain of failures.


Stability ===

CrackStoppers - failures will happen, you have the ability to desing your system's reaction to specific failures. Just like auto engineers create crumple zones - areas designed to protect passenfers by failing first - you can create failures modes that contain the damage and protect the rest od the system


The more tightly coupled the architecture, the grater the chance an error can propagete. Conversely, te less coupled architectures  act as shock absorbers, disminishng the effect od this error insted of amplifying them.

What are all the ways this can go wrong?
Preserve partial functionality insted of allowing total crashes.


Blocked Threaded - Connection Pools - Your app will scale better if request handling threads never block each other

Size Resource poll to request thread pool, don use code for content. 

Sessions are th eachiless helel of every application server.

URL Rewriting to track sessions, each request will create a session

