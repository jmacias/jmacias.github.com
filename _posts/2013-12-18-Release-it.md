---
layout: post
title: On "Release it".
published: true
---

["Release It"][Release-it] by Michael Nygard has been forever in my to-read list, not until now I need it the most. With DevOps methodology rising, I ended up more involved
 with the support of a production system that I also help develop. In that moment the Book was a mandatory read for me.

## What they do not teach in school.

>Statistics gurantee that the majority of programmers have nerver worked on really large, mission-critical software.  First, salary surveys consistently show that most programmers have less than ten years of experience. Second the histogram of project sizes is heavely weighted toward the smaller end of the scale. So, take a young population with the relatively few opportunities to work on a giant projects, and it's not surprice that experience at that level is hard to find. 
>
>These issues certainly aren't covered in colleges and universities. Where optimization regards to tweaking up some search algorithm.


That alone is the main reason why I am happy I read the book. As mentioned several time in the book, __getting your application to ship is only half the battle__. Your application still has to survive in the field, with failing integration points, high peak  of concurrent users or slow responses from a third party web services. This book is packed with expirience and advices to __make your application ready to survive "production"__. 


## Misconceptions tackle by the book

   * You need accept the fact that despite your best laid plans, bad things will happen.
   * Realize that "Release 1.0" is not the end of the development project but the begining of the system's life on its own.

### Patterns and Antipatterns for Production ready software

Antipatterns:

   * Slow Response
   * Blocked Threads
   * Integration Points - Number one killer of systems, without timeouts, is a surefire way to create cascading failures or accelerate cracks in a system.
   * Chain Reactions
   * Cascading Failures
   * Unbalanced Capacities
   * Unbounded Resultsets
   * Atttacks of Self Denial

Patterns:

   * Bulkheads as a tool for Damage containment. Like in ships, bulkheads prevents water from moving from one section to another avoiding the ship to sink.
   * Decoupling middleware. Avoid many failures modes through total decoupling. Learn many architectures and chose among them, __Not every system needs to look like a three-tier application with an Orable Database. Learn many architectural styles and select the best architecture for the problme at hand__.
   * Circuit Braker
   * Use Timeouts
   * Fail Fast 
   * Handshaking

## Quotes

Some great quotes I gather from the book:

>__Design and architecture decisions are also financial decisions__. These choices must be made with and eye toward their implementation cost as well as their downstream costs

----

>In the world of bussines it all come down to money. Systems cost money. And to stay in bussines, you need to make money.

----

>Why Agile? Their emphasis on early delivery and incremental improvements means software gets into production quickly. Since production is the only place to learn how the software will repond to real-world stimuli. __I avocate any appproach that begins the learning process as soon as possible__.

----

>Enterprise Software systems - enterprise class symple means that the software must be availbale , or the company loses money.

----

>__Bugs will happen. They cannot be eliminated, so they must be survived insted__.

----

>I realized that the development team were building everything to pass testing, not to run in production.

---

One of the biggest lesson from the book:

>__The funsion of technical and financial viewpoints__ is one of the most important recurring themes in this book.

## Go Read The Book.

The book is a classic and a must read for any developer. Full of knowledge and expirience is a good way to get familiar with the problems faced in production enviroments, that not everyone in the software development world get the opportunity to experience. I left the best book quote for the end:

>__The true birth of a system comes not on the day that design and development begins, or even when the project is conceived, but on the day it launches into production. This is a beginning, not an end. Over time, the system will grow and mature. It will gain new features. It will lose defects, and perhaps gain some too. It will become what it was meant to be, or, even better, it will become what it needs to be. Most of all, it must change. As system that cannot adapt to its environment is stillborn.__


[Release-it]: http://pragprog.com/book/mnee/release-it "Release it by Michael Nigard"
