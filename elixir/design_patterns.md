### How Design patterns look in Elixir: 

1) Mediator
    Examples: Phoenix Controller, Phx LiveView
    Solutions:
    - Funcs and modules for controlling and coordinating logic
    - Processes for controlling and coordinating events

2) Facade
    Examples: Phx Contexts, Logger, Elixir compiler
    Solutions: Modules prociding a simplified API to the more general facilities of a subsystem

3) Strategy
    Examples: 
    Solutions:
    - Pattenr matching
    - Anon functions
    - Interfaces from OO a.k.a Protocols in Elixir
    -- interfaces are a mechanism for polymorphism (with upfront contract)"(c) José Valim
    Polymorphism in Elixir:
        Behaviour == Modules
        State == Data
        Mutability == Processes

    "Favor object composition over class inheritance"(c) Gang of Four

Source: https://www.youtube.com/watch?v=agkXUp0hCW8
