---
pubDate: 2024-08-23
author: David Hérault
title: How to build a tech product fast
description: "If you read only this line, here is the pitch: you don’t care about the tech stack or architecture yet, choose whatever tech allows you to iterate faster."
image:
  url: "/images/tech-products.png"
  alt: "#"
tags: ["Tech", "React", "Building", "Frontend", "Backend", "Database"]
---

If you read only this line, here is the pitch: you don’t care about the tech stack or architecture yet, choose whatever tech allows you to iterate faster. The outcome will be beneficial for your venture, the problems that will arise later from your choices are future-you’s or your future CTO’s.


Dear builder,

It is with great joy that I give you this 2024 framework for building technological products faster.

My main point is the following: you should not choose a tech stack based on liking or previous experience with technology. You should choose whatever iterates faster. So, with no further ado, here is a list of common technologies and their common mistakes.

## Frontend framework

This blog post will not end the war between React, Vue, Angular, etc..

The fact is you want to go fast, so contrarily to what has just been said, pick the one you know better and stick with it.

But if you’re a beginner or a jack of all trades, pick React, because hiring will be cheaper later on. Also, the community is larger, and the support is definitely long-term.

## Frontend features

Need a calendar? Use a library for that, don’t build your own.

Need a video chat? Use a paid third-party API such as Daily unless you’re a WebRTC expert.

Need a static website? Use Webflow or the equivalent, even if you’re the best frontend dev around. You will go 10x faster.

The main point is to use existing products instead of creating your own. Yes, we are artists, but letting these artistic vibes go until you have more time and money, and human resources to express them will save you a lot of time.

## Backend solutions

Go serverless. Period.

As the creator of [serverless-offline](https://github.com/dherault/serverless-offline), I am well placed to tell you that this is the time-effective solution. Plus, it costs way less than other solutions at smaller scales. But, again, going Kubernetes or otherwise will be a problem for the future.

Monolithic backends are not only costly, but they also require a lot of no-code management and are code-greedy. Be careful here.

I am recommending Google Cloud Platform’s Cloud Run, the best-in-class solution for serverless applications as of now, in my opinion.

## Database

Use Firebase’s Firestore or the equivalent. Why? Free real-time, no need for a time-consuming Websockets environment! You might argue that it costs a lot after some usage, but if you ever make it to this point, congratulations, you made it.

Traditional databases such as PostgreSQL require a backend, which means going REST or GraphQL to communicate with the frontend. If you somehow manage to elude this, you will save 50% of the dev time.

## Hosting

You might be an old-school Nginx DevOps kind of person, in that case, you may take that building opportunity to learn something new. Nowadays, static assets handling is easy as 1 2 3.

Simply use Firebase or Netlify hosting solutions to deploy with ease. They integrate nicely with your CI.

Buckets and load balancers should not be part of your tech stack if your plan is to go fast.

## Continuous Integration

GitHub actions, GitLab CI or Netlify should be your goal here. Other solutions are either not free or too code-greedy. Again, it is hard to reinvent CI, but you can still lose some precious hours trying to make it yours.

## Conclusion

Engineering is hard. The choices you make at the beginning of a project can mean life or death for your product. Stop being a full-time engineer, start doing user research and marketing your priorities as a product builder.

Thank you, and have fun building fast.
