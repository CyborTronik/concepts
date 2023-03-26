---
layout: post
title:  "Re-structured Architecture Types By Domain"
date:   2023-03-19 20:26:08 +0000
categories: categories domain
---
A common expectactation for the software in business terms is to be a `solution` of certain `situation`.
And it makes a natural fit for the software design to be shaped around the bussiness domain and meaning. In otherway define type of architecture where the pivot (north-star) is the business domain.

In this regard the suggestion is to look at commonly used terms in the following way:

| Solution Scope | Type |
| ----------- | ----------- |
| Full business scope + End to end solution | *Monolithic Architecture* |
| Full business scope + One layer | *Layered Architecture* [^1] |
| Bounded domain + End to end solution | *Service Oriented Architecture (SOA)* [^2] |
| Bounded domain + One layer | *Micro application* [^3] |

**Note:** *Event based* system is a way of interaction and less about domain, therefore not included here. Which could be a valid architecture type, but needs a different pivot for categorization. See [Communication Types]({{site.baseurl}}{% post_url 2023-03-25-communication_types %}) for more details.

[^1]: For layered architecture a popular case is Client-Server one. Where `Client` is considered as one layer that knows everything in the business scope. And the `server` as another layer that knows the whole business context too.
[^2]: SOA at times might be considered monolithic architecture when the context is either not bounded or too big to handle.
[^3]: More comonly is *microservice* which is about backend side, while on the front end you may find the term *micro frontend*.
