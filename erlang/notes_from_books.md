## Notes from books.

source: Learn you Erlang for great good
link: local, PDF
notes:

Chapter 10.
- Erlang devs decided to avoid shared memory for all process. Each process "clones" needed data into own memory. If (and when) the process fails - no other process impacted (no process had access to the process' memory). This way, messages between processes contain those data which need to be cloned for each particular process.
It might be slower, but highly safe and will endure;
- Early Erlang developers keep in mind that deniels/failures are usual things for every service.
- awesome idea from Erlang: it's better to develop best ways possible to handle errors and failures instead of developing ways to prevent those mistakes
- async messaging. Process A sends a message to Process B's mailbox without any validation (whats inside of the message, does mailbox exist etc). Process B reads from own mailbox. 




---

source: CRASH-ONLY SOFTWARE AND MICROREBOOT: A DESIGN AND TECHNIQUE FOR ACHIEVING HIGH AVAILABILITY IN FREQUENTLY-FAILING SOFTWARE SYSTEMS. A DISSERTATION
link: https://dslab.epfl.ch/pubs/phd-candea.pdf
notes:
The exact root cause of these failures is often unknown and the only cure is to reboot

The fast, minimally-disruptive nature of microrebooting makes several failure management policies cost-effective, policies that would otherwise be prohibitively expensive in terms of incurred downtime
