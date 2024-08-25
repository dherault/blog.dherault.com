---
pubDate: 2024-08-24
author: David Hérault
title: Building Arccode.dev
description: "It took me 15 days to build Arccode.dev, here is how I did it."
image:
  url: "/images/arccode.png"
  alt: "#"
tags: ["Tech", "React", "Building", "Frontend", "Database"]
---

It took me 15 days to build [Arccode.dev](https://arccode.dev), here is how I did it:

## What is Arccode

Arccode is a role-playing game for developers. It turns the keywords you type while coding (such as `function` or `const`) into experience points. The more you code, the more you level up. By leveling up you can unlock items and avatars to customize your character. It is a fun way to track your progress and stay motivated while coding.

## Frontend only

Arccode is a frontend-only project. There is no backend attached to it, but simply a collection of Firebase functions, based on Google Cloud Run. Its serverless nature allowed me to iterate very quickly and made the whole project easy to develop. Firebase is a great solution for solo developers looking to iterate quickly.

A good Firebase frontend-only project should have strict security rules for Firestore. Firestore is a realtime database, and works with a set of rules written by the developer that define how the data can be accessed or modified. I had to limit to the maximum the user’s possibilities so that the app stays secure and prevents cheating. Here is an example of such rules preventing the user to affect protected fields:

```jsx
function isNotAffectingCharacterProtectedFields() {
  return !request.resource.data.character.diff(resource.data.character).affectedKeys().hasAny([
    'level',
    'keywordRegistry',
    'levelUpKeywordRegistry',
    'lastDailyRecapKeywordRegistry',
    'unlockedItems',
  ])
}

```

As you can see their is no margin for hacking the product. Note that rules are bypassed when executing the query inside of a serverless function, which is great as it allows to perform administrator queries easily. In a nutshell creating a frontend-only app is a game changer from the traditional frontend ↔ backend paradigm. The time spent coding is divided by half, so long REST APIs!

## VSCode extension

Arccode works with a VSCode extension. The extensions reads the keywords inputed by the developer and sends the count to a serverless function. In no way does it send the full code to the server.

Writing a VSCode extension was new to me. I found a good tutorial online on how to handle the custom authentication flow with https://arccode.dev, the rest was easy. To handle the keyword counting, I used a previous project called “array-differences”, a NPM package that can diff an array of m length with an array of n length with a m * m * n complexity. Not optimal but good enough to diff lines of code changes in a VSCode text editor. After a few days of testing the v1 was shipped, hooray!

## Marketing

Arccode is a pet project, not something too serious. To market it I placed a sponsoring message on my most popular project: serverless-offline. This library is downloaded half a million times a week and can drive real traffic the arccode.dev. Here is what the message looks like:

![serverless-offline sponsoring](/images/arccode-sponsor.png)

I sincerely hope that serverless-offline users will not be too put off by the message. If it causes lots of complains, I will remove it.

I also spent a few days working on the landing page. I wanted it to convey a strong message about Arccode, one that speaks to the heart of its viewers. So I made it as pretty as I could and really insisted on the wording. Landing pages are important, work on them.

## Conclusion

Arccode was a fun project to develop, I enjoyed every moment of it. I hope it will bring joy to its users, and that it can continue to grow with time. Pet projects are important for every developer: it is an efficient way to increase one’s skills and show the world what you can do.

Let me know what you think of Arccode by sending me an email, it would be my pleasure to read from you.

Best,
