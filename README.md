# Independent Service Heuristics

Rules-of-thumb (clues) for identifying candidate value streams and domain boundaries by seeing if they could be run as a separate SaaS/cloud product. Based on some of the ideas in the book _Team Topologies_ by Matthew Skelton [@matthewskelton](https://github.com/matthewskelton) and Manuel Pais [@manupaisable](https://github.com/manupaisable).

> See [teamtopologies.com](https://teamtopologies.com/) for more details about Team Topolologies.

> Copyright © 2018-2020 [Team Topologies](https://teamtopologies.com/) - Licenced under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) ![CC BY-SA 4.0](https://licensebuttons.net/l/by-sa/3.0/88x31.png)

## Overview

When designing organizations for fast flow of change, we need to find effective boundaries between different streams of change. Techniques like Domain Driven Design (DDD) are very powerful for this, but can be quite involved and difficult to learn. An lightweight intermediate approach is to ask "could this thing be run as a cloud-hosted (SaaS) service or product?". 

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
