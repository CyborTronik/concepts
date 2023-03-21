---
layout: post
title:  "Simplified Architecture Types By Domain"
date:   2023-03-19 20:26:08 +0000
categories: categories domain
---
A common expectactation for the software in business terms is to be a `solution` of certain `situation`. 
And it makes a natural fit for the software design to be shaped around the bussiness domain and meaning.

In this regard the suggestion is to look at commonly used terms in the following way:

| Solution Scope | Type |
| ----------- | ----------- |
| Full business scope + End to end solution | *Monolithic Architecture* |
| Full business scope + One layer | *Client-Server Architecture* [^1] |
| Bounded domain + End to end solution | *Service Oriented Architecture (SOA)* [^2] |
| Bounded domain + One layer | *Micro application* [^3] |


[^1]: `Client` considered as one layer that knows everything in the business scope. And the `server` as another layer that knows the whole business context too.
[^2]: SOA at times might be considered monolithic architecture when the context is either not bounded or too big to handle.
[^3]: More comonly is *microservice* which is about backend side, while on the front end you may see the term *micro frontend*.
