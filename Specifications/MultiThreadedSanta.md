# The Multi-threaded Santa TDD Challenge

PLEASE GO TO [CODEMANSHIP](http://codemanship.co.uk/parlezuml/blog/?postid=1337) FOR THE ORIGINAL ARTICLE.

## Background Info

## Specification

## Test Data

## Use Case Scenarios

If you've hunted on the Interwebs for TDD katas, you will no doubt have noticed that they tend to be based on relatively straightforward problems. In particular, there are no - as far as I'm aware - TDD katas that set more challenging high-volume, multi-threaded, multi-process problems to solve.

In the spirit of Christmas - if you celebrate such a thing (and this year, I won't be) - I set some students just such a problem, which I'm calling the Multi-threaded Santa TDD Challenge.

Now, read this very carefully. It goes something like this:

Multi-threaded Santa TDD Challenge


Goal


The goal is to make, wrap, load and deliver 1 million presents on Xmas Eve. Play this challenge in pairs, with multiple pairs competing to do it for the lowest cost.

Problem


Santa and his elves have to make, wrap, load and deliver 1 million presents. They work in 4 teams:

1. Making

2. Wrapping

3. Loading

4. Delivering

Each team must be implemented in its own process (e.g, a web service for each activity, or a daemon, etc etc).

Each team either sends to or takes from (or both) one of 4 queues, and each queue has a maximum size, beyond which no more presents can be added:

1. Made (max size = 1000)

2. Wrapped (max size = 2000)

3. Loaded (max size = 5000 - these are all the presents on Santa's sleigh for delivery)

4. Delivered (no size limit)

How does Santa deliver all those presents in just one night, though? Simple. Santa Time works differently to our time. An hour in Santa Time is just 1 second (1,000ms) of human time. So 3600 hours of Santa Time elapse in 1 hour of human time.

You must implement these time delays in a Present class, with 4 distinct lifecycle event methods:

* Present.make() - wait 50ms

* Present.wrap() - wait 10ms

* Present.load() - wait 5ms

* Present.deliver() - well, we'll get to that...

To perform work on a present, a worker thread must invoke the appropriate method, incurring a time cost for that work within that thread. Only after that work has been performed can the present be sent to the queue for the next process to take from. e.g. one thread in the Making process called present.make(), then sends that present to the Made queue, where the Wrapping process can pick it up.

In each process, there are one or more elves (worker threads). Elves are managed by a fifth process: the Elf Pool. To add an elf (worker thread) to a process (e.g., wrapping), you must request an Elf ID from the Elf Pool.

The Elf Pool records every elf assigned to every process for the duration of the work.

Because of the very strict rules of the Elf Union, elves - once assigned to the work - cannot be laid off. So the total number of elves employed can only go up, not down, until all presents have been delivered.

Re-assigning Elves:

Elves can, however, be swapped between the 4 work processes: so an elf assigned to wrapping can be re-assigned to loading, for example. This, too, must be managed through the Elf Pool. 

One worker process (e.g. wrapping) signals an intention to reassign one of its elves to the Elf Pool. The elf remains in that process until another worker process (e.g., Loading) requests another elf, at which point - instead of assigning a new elf from the pool - that elf is re-assigned instead. So the total number of elves employed remains the same. If the Elf Pool has no elves awaiting re-assignment, it assigns a new elf when one is requested.

There is only one Santa, and only one sleigh! 

Okay, here's your bottleneck. There can only be one worker thread in the Delivering process, and the delivery round takes a fixed amount of time each time the sleigh goes out, regardless of how many presents or elves are assigned to Delivery. It takes Santa 500ms to make one round of deliveries. i.e. delivering all the presents on Santa's sleigh - no matter how many there are - incurs a time delay of 500ms. At the end of that time, all the presents in the sleigh (i.e., on the Loaded queue) are delivered. This could, for example, be achieved with a Sleigh class that implements the time delay in a deliver() method.

Be advised that no presents can be loaded for delivery while Santa's sleigh is out on a round. This is your bottleneck! For 500ms (at least), the elves doing the loading will be idle. So you may want to reassign them to making or wrapping. But... hmmm... how long will that take?

How to score?

The Elf Pool has another job in this challenge: elves don't work for nothing. They work for cookies. Specifically, one elf assigned for one hour of Santa Time (1s of human time) gets paid 1 cookie. So 100 elves assigned for 1000s of human time would cost 100,000 cookies.

The Elf Pool calculates the cookie payroll, multiplying the number of assigned elves by the time it takes to deliver all the presents in human seconds.

To win, your team needs to deliver all 1 million presents for less cookies than your competitors.

Never Give In. Never Surrender.

Now, here's the kicker: once the start whistle blows, there is NO STOPPING. If any of your worker processes falls over, the work becomes blocked, the clock keeps on ticking, and you keep burning cookies. Restarting any worker process must re-attach all of the elves that were assigned to it via the Elf Pool before it can begin working on presents again.

If your Elf Pool falls over: you are disqualified, and Santa gets to kick you in the backside for all eternity for ruining Xmas!!!

So, there you have it: 1 million presents, 4 worker processes, as many worker threads as you like (within the rules), 4 work queues, and one manager process keeping track of the elves and the cookies and the time.

Easy as cheese. Average time for students to complete was 4 hours. My advice: keep it as simple as you can. I've already piled on plenty-much complexity for you to deal with!
