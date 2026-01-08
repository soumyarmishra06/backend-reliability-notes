# Simplifying Distributed Systems Improves Reliability

One recurring lesson from operating backend systems in production is that reliability often improves more by simplifying system structure than by adding new safeguards.

In several systems I’ve worked on, initial responses to reliability issues included:
- Adding retries
- Increasing timeouts
- Introducing additional fallback paths

While these helped in specific cases, the largest reliability gains came from reducing:
- The number of synchronous dependencies
- Hidden coupling between services
- Overly generic abstractions

Simplification reduced failure propagation and made operational behavior easier to reason about during incidents.

This also improved on-call experience, as fewer components needed to be understood under pressure.

The trade-off was sometimes reduced flexibility, but in long-lived systems this was usually acceptable.

**Takeaway:**  
Designing for operability is as important as designing for functionality.
