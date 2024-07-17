## Supervisors

I know static Supervisor. We have two more supervisor `DynamicSupervisor` & `PartitionSupervisor`

DynamicSupervisor support to add child at runtime (on demand) through start_link/1.
This type of supervisor support us can add dynamic task (process) depend input.
But **downside** of this type is missed :one_for_all & :rest_for_one strategy.

For fix bottleneck (what?) of DynamicSupervisor we go to using PartitionSupervisor.

PartitionSupervisor is one of different to original Erlang supervisor. It uses number of processes (can config, default is equal to number of schedulers of Erlang VM). Each process is a partition and when add new child supervisor uses key for calculating partition child will go to start on.




