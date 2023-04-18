# Independent Service Heuristics

The Independent Service Heuristics (ISH) are rules-of-thumb (clues) for identifying candidate value streams and domain boundaries by seeing if they could be run as a separate SaaS/cloud product. Based on some of the ideas in the book _Team Topologies_ by Matthew Skelton [@matthewskelton](https://github.com/matthewskelton) and Manuel Pais [@manupaisable](https://github.com/manupaisable).

> See [teamtopologies.com](https://teamtopologies.com/) for more details about Team Topolologies.

> Copyright © 2018-2021 [Team Topologies](https://teamtopologies.com/) - Licenced under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) ![CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/3.0/88x31.png)

## Overview

When designing organizations for fast flow of change, we need to find effective boundaries between different streams of change. Techniques like Domain Driven Design (DDD) are very powerful for this, but can be quite involved and difficult to learn. A lightweight intermediate approach is to ask "could this thing be run as a cloud-hosted (SaaS) service or product?".

The ISH approach covers many typical situations in modern software but not all. It's designed to stimulate conversation and provide a frame for thinking, not as a perfect "catch-all" tool.

## How to use

Choose an area of the organisation's focus to be represented in software: a user journey, a "product", a possible business domain, a software service, an entire software application, a set of tasks for a single user persona, a possible value stream, etc.

Use the checklist below to ask questions about the candidate domain / service / application / value stream. The more "yes" or "probably" answers, the greater the chance that you have found a good candidate for being a separate stream of change. This means that we could arrange one or more Stream-Aligned teams to this area.

## Checklist

1. **Sense-check**: Could it make any logical sense to offer this thing "as a service"?
    - Is this thing independent enough?
    - Would consumers understand or value it?
    - Would it simplify execution?
2. **Brand**: Could you imagine this thing branded as a public cloud service (like _AvocadoOnline.com_ 🥑)?
    - Would it be a viable business (or "micro-business") or service?
    - Would it be a compelling offering?
    - Could a marketing campaign be convincing?
3. **Revenue/Customers**: Could this thing be managed as a viable cloud service in terms of revenue and customers?
    - Would it be viable service with a paid offering?
    - Would it bring recurring revenue with subscription plans?
    - Is there a clearly-defined customer base or segment?
4. **Cost tracking**: Could the organisation currently track costs and investment in this thing separately from similar things?
    - Are the full costs of running this thing transparent or possible to discover considering infrastructure costs, data storage costs, data transfer costs, licence costs, etc.?
    - Is this thing fairly separate, disconnected from other things in the organisation?
    - Does the organisation track this separately?
5. **Data**: Is it possible to define clearly the input data (from other sources) that this thing needs?
    - Is the thing fairly independent from any data sources?
    - Are the sources internal (under our control, not external)?
    - Is the input data clean (not messy)?
    - Is the input data provided in a self-service way? Can the team consume the input data "as a service"?
6. **User Personas**: Could this thing have a small/well-defined set of user types or customers (user personas)?
    - Is the thing meeting specific user needs?
    - Do we know (or can we easily articulate) these user types and their needs?
7. **Teams**: Could a team or set of teams effectively build and operate a service based on this thing?
    - Would the cognitive load (breadth of topics/context switching) be bounded to help the team focus and succeed?
    - Would significant infrastructure or other platform abstractions be unnecessary?
8. **Dependencies**: Would this team be able to act independently of other teams for the majority of the time to achieve their objectives?
    - Is this thing logically independent from other things?
    - Could the team "self-serve" dependencies in a non-blocking manner from a platform?
9. **Impact/Value**: Would the scope of this thing provide a team with an impactful and engaging challenge?
    - Is the scope big enough to provide an impact? Would the scope be engaging for talented people?
    - Is there sufficient value to customers and the organization that the value would be clearly recognized?
10. **Product Decisions**: Would the team working on this thing be able to "own" their own product roadmap and the product direction?
    - Does this thing provide discrete value in a well-defined sphere of execution?
    - Can the team define their own roadmap based on what they discover is best for the product and its users (so that the team is not driven by the requirements and priorities of other teams)?

## Further considerations

* **Vocabulary**: is the vocabulary consistent between different parts of the system or different business domains? If not (if the same word means something different in different areas), then there may need to be two different services or systems.
* **Phases**: does one part of a system deal with an earlier or later phase in processing? This may also represent a good boundary.
* **Wardley Maps**: could the capability or service be outsourced to a SaaS Product or Commodity provider? Will it likely be outsource-able soon? If so, it's a candidate for splitting off as a separate service in preparation for possible outsourcing to a Product or Commodity provider.
* **Risk**: what is the cost of risk of splitting this capability or service? Could something go wrong?

### Detailed considerations

* **Loose coupling**: Does this 'thing' make sense to independently migrate / deploy in the public cloud independent of related 'things'?
* **Tight coupling**: Do you have any dependencies on vendor / 3rd party software that prevents scaling if demand increases ?
* **Commercial opportunity**: Is there demand for this 'thing' outside of the context of its current usage? Could this be used more broadly within your organization or to different customer segments?
* **Data governance**: Does this 'thing' act as a master or authoritative source for key static / reference / client data?
* **Interface contracts**: Do you have versioned interface contracts and the ability to deploy new versions without impacting existing 'customers' (consumers)?
* **Resilience / scalability**: as demand for your 'thing' scales do you have a linear increase in demand for new capacity / availability (including geographical regions)?
* **Skills liquidity**: consider the skills mix in the teams. Can the teams each own their service/system after the split?
* **Anti-pattern - data coupling**: Does your 'thing' depend upon tight coupling / specific vendor drivers or use things like DB Links rather than through a managed versioned API?
* **Anti-pattern - release coordination**: Do you upstream / downstream producers / consumers need your 'thing' to coordinate a release (e.g. release train) or can they release independently as frequently as they need to?

## Resources

* Watch [Matthew Skelton](https://github.com/matthewskelton) and [Nick Tune](https://github.com/ntcoding)'s [talk on ISH from DDD Europe 2022](https://www.youtube.com/watch?v=q8hwkDyL6Zs)
* Read more about [Team Topologies](https://teamtopologies.com/key-concepts)
* Explore [Domain-Driven Design Heuristics](https://www.dddheuristics.com/) - part of the excellent [virtualDDD.com](https://virtualDDD.com/) community
* Learn how to use [Event Storming](https://techbeacon.com/devops/introduction-event-storming-easy-way-achieve-domain-driven-design) to discover different business domains - this can be a good 'bridge' to Domain-driven Design (DDD) - _thanks to [Rebecca Wirfs-Brock](https://twitter.com/rebeccawb) for this insight_
* Discover [Wardley Maps](https://hiredthought.com/2018/09/01/intro-to-wardley-mapping/)
* Read about [Skills Liquidity by Chris Matts](https://theitriskmanager.com/2013/11/24/introducing-staff-liquidity-1-of-n/)

## Acknowledgments

> Thank you to the people at the [DDD London meetup group](https://www.meetup.com/dddlondon/events/265895638) for their input on an early version of the Independent Service Heuristics. 😻

Thanks also to:

* [Nick Tune](https://github.com/ntcoding) and the [DDD Crew](https://github.com/ddd-crew) for awesome DDD resources
* [Kacper Gunia](https://github.com/cakper) for the invitation to speak at DDD London meetup
* [all contributors to this repository](https://github.com/TeamTopologies/Independent-Service-Heuristics/graphs/contributors)
