## DDD. Integration patterns

> "...all integration patterns between bounded contexts: https://opus.ch/ddd-concepts-and-patterns-context-map/. You almost never want to be a conformist if not both services are in your direct control. Add anticorruption layer to be safe..."(c) 

> "But be aware: integration patterns are not strictly technical but sociotechnical, so integration which takes into account the technical stuff and people and communication between people..."(c)


### DDD Integration patterns
- Customer/Supplier
- Shared Kernel
- Open Host Service
- Published Language
- Anticorruption Layer
- Conformist
- Separate Ways

---

Most interesting for now is:
Anticorruption Layer
If we have no control over the context we would like to connect to, and its model doesn’t fit ourselves an anticorruption layer should be considered. This layer communicates with the other context in its language and translates from and to it.

The anticorruption layer can be especially useful when migrating a legacy system. It encapsulates the legacy system, and our new shiny solution communicates only with this layer in a clean language.

Level of communication and commitment: Low
Level of control over the involved systems: Low
