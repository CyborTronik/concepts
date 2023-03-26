---
layout: post
title:  "Re-structured Communication Types"
date:   2023-03-25 23:59:00 +0000
categories: communications events async
---

An imense amount of books and sources have missalignments in the way of mixing the [software architecture types]({{site.baseurl}}{% post_url 2023-03-19-architecture_type_by_domain %}) with the way communication and have it in one backet as "Categories of Architecture".

To avoid that confusion in addition to the [re-structured software architecture types]({{site.baseurl}}{% post_url 2023-03-19-architecture_type_by_domain %}) below is the concise suggestion of the ways of interaction between system or software artifacts.

Kind of software interactions:

| Type | Alias/Reference | Attributes |
| ---- | ---------------------- | ---------- |
| *Blocking request* | syncronious communication | Blocked process untill gets the result. |
| *Async request* | asyncronious communication | Blocking request that gets a reference ID immediately, and multiple requests after that (pulling), that checks the result based on the reference ID. |
| *Notify request* | event based communication, also fire and forget [^1] | One way communication. A kind of request that doesn't wait for response. |
| *Subscriber* | event based communication | Actually only receiving **responses** not requesting them. Low load, eventual consistency. |
| *Realtime processing* | streaming | Pulling (almost listening) or push-based data and receiving results as soon as they are ready to be processed. |
| *Bulk processing* | batch jobs | One time processing of big amount of data. Resource hungry. Has eventual consistency. |

[^1]: Fire and forget concept usually goes togheter with the [Actor based systems](https://doc.akka.io/docs/akka/current/typed/interaction-patterns.html#fire-and-forget), an evolution of the concept from [Erlang lang](https://www.erlang.org/).