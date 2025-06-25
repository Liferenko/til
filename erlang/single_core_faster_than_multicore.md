## erl -smp disable

In some cases, multicore might make our app slower than on signle core.
from book "learn you some Erlang for great good"
"...sometimes when code contains a lot of sequential algorithms - at this point, multicore shoots you in your leg"

Solution: `erl -smp disable`

UPDATE: seems like `-smp disable` is outdated. help said "use `erl +S 1` to start erl with 1 run queue. Accordingly, +S 10 starts 10 queues
