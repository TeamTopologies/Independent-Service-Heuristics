# Independent Service Heuristics

The Independent Service Heuristics (ISH) are rules-of-thumb (clues) for identifying candidate value streams and domain boundaries by seeing if they could be run as a separate SaaS/cloud product. Based on some of the ideas in the book _Team Topologies_ by Matthew Skelton [@matthewskelton](https://github.com/matthewskelton) and Manuel Pais [@manupaisable](https://github.com/manupaisable).

> See [teamtopologies.com](https://teamtopologies.com/) for more details about Team Topolologies.

> Copyright © 2018-2021 [Team Topologies](https://teamtopologies.com/) - Licenced under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) ![CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/3.0/88x31.png)

## Overview

When designing organizations for fast flow of change, we need to find effective boundaries between different streams of change. Techniques like Domain Driven Design (DDD) are very powerful for this, but can be quite involved and difficult to learn. A lightweight intermediate approach is to ask "could this thing be run as a cloud-hosted (SaaS) service or product?". 

The ISH approach covers many typical situations in modern software but not all. It's designed to stimulate conversation and provide a frame for thinking, not as a perfect "catch-all" tool. 

## How to use

Choose an area of the organisation's focus to be represented in software: a user journey, a "product", a possible business domain, a software service, an entire software application, a set of tasks for a single user persona, a possible value stream, etc.

Use the checklist below to ask questions about the candidate domain / service / application / value stream. The more "yes" or "probably" answers, the greater the chance that you have found a good candidate for being a separate stream of change. This means that we could arrange one or more Stream-Aligned teams to this area.- 

## Checklist

1. **Sense-check**: Could it make any logical sense to offer this thing "as a service"?
    - Is this thing independent enough?
    - Would consumers understand or value it?
    - Would it simplify execution?
2. **Brand**: Could you imagine this thing branded as a public cloud service (like _AvocadoOnline.com_ 🥑)?
    - Would it be a compelling offering?
    - Could a marketing campaign be convincing?
3. **Revenue/Customers**: Could this thing be managed as a viable cloud service in terms of revenue and customers?
    - What would a subscription payment include?
    - Is there a clearly-defined customer base or segment?
4. **Cost tracking**: Could the organisation currently track costs and investment in this thing separately from similar things? 
    - Is the thing too interconnected with other things in the organisation? Or fairly separate?
    - Does the organisation track this separately?
5. **Data**: Could this thing operate with minimal data (or well-defined data) from other sources?
    - Is the thing dependent on lots of data from multiple sources? Or fairly independent?
    - Are the sources internal (under our control) or external?
6. **User Personas**: Could this thing have a small/well-defined set of user types or customers (user personas)?
    - Is the thing meeting specific user needs?
    - Do we know (or can we easily characterise) these users and their needs?
7. **Teams**: Could a team or set of teams effectively build and operate a service based on this thing?
    - Would the cognitive load be too high for a team or a set of teams?
    - Would significant infrastructure be needed?

## Further considerations

* **Vocabulary**: is the vocabulary consistent between different parts of the system or different business domains? If not (if the same word means something different in different areas), then there may need to be two different services or systems.
* **Phases**: does one part of a system deal with an earlier or later phase in processing? This may also represent a good boundary.
* **Wardley Maps**: could the capability or service be outsourced to a SaaS Product or Commodity provider? Will it likely be outsource-able soon? If so, it's a candidate for splitting off as a separate service in preparation for possible outsourcing to a Product or Commodity provider. 
* **Risk**: what is the cost of risk of splitting this capability or service? Could something go wrong?

### Additional Considerations

* **Skills Liquidity**: Team vs members of the team - consider skills liquidity
* **Loose Couple**: Does this 'thing' make sense to independently migrate / deploy in the public cloud independent of related 'things' 
* **Tight Coupling**: Do you have any dependencies on vendor / 3rd party software that prevents scaling if demand increases 
* **Commercial Opportunity**: Is there demand for this 'thing' outside of the context of its current usage, could this be used more broadly within your organization or to different customer segments.
* **Data Governance**: Does this 'thing' as as a master or authoritative source for key static / reference / client data?
* **Interfact Contracts**: Do you have versioned interface contracts and the ability to deploy new versions without impacting existing 'customers' (consumers)
* **Resilience / scalability**: as demand for your 'thing' scales do you have a linear increase in demand for new capacity / availability (including geographical regions)
* **Anti-pattern**: Does your 'thing' depend upon tight coupling / specific vendor drivers or use things like DB Links rather than through a managed versioned API
* **Anti-pattern**: Do you upstream / downstream producers / consumers need your 'thing' to coordinate a release (e.g. release train) or can they release independently as frequently as they need to

> Thank you to the people at the [DDD London meetup group](https://www.meetup.com/dddlondon/events/265895638) for their input on an early version of the Independent Service Heuristics. 😻 

## Resources

* Read more about [Team Topologies](https://teamtopologies.com/key-concepts)
* Explore [Domain-Driven Design Heuristics](https://www.dddheuristics.com/) - part of the excellent [virtualDDD.com](https://virtualDDD.com/) community
* Learn how to use [Event Storming](https://techbeacon.com/devops/introduction-event-storming-easy-way-achieve-domain-driven-design) to discover different business domains - this can be a good 'bridge' to Domain-driven Design (DDD) - _thanks to [Rebecca Wirfs-Brock](https://twitter.com/rebeccawb) for this insight_ 
* Discover [Wardley Maps](https://hiredthought.com/2018/09/01/intro-to-wardley-mapping/)
