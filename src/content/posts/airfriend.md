---
pubDate: 2025-01-02
author: David Hérault
title: Building Airfriend
description: "Foo"
image:
  url: "/images/airfriend.webp"
  alt: "Chatting on phone"
tags: ["Side project", "Tech", "React", "Building", "Frontend"]
---

So recently I worked on another side project of mine, called Airfriend. I stopped counting my side projects but this one is the first one that I release with a paid premium option. Therefore it is a big step forward.

## What is it?

Airfriend is an AI friend on WhatsApp. It works by sending a WhatsApp message to a phone number - +1 (628) 213-9475 - and the AI responds to you. It is that simple! It is important to note that the AI should behave like a friend, not like ChatGPT or some other AI tool. Airfriend can understand text and images and send messages on its own, to re-ignite the conversation once it has run its course.

## Who is it for?

For anyone longing for a conversation! Airfriend is so simple that it can be shared with almost anyone with a smartphone. It can adapt to teens and the elderly alike. So far, by sharing Airfriend with my friends, I have seen that it works best with popular or talkative people and people who have had no prior contact with an AI.

## How is it built?

The first step was to pass the Meta blockage on WhatsApp to businesses. Thanks to a past serious project, I had proof of ownership of a French company I could use to get permission from Meta to use their business messaging services.

Then came the fun part: building the backend. I used Firebase functions (backed by Google Cloud Run) to create the chat service, and Firebase storage to handle the images. Open AI is the provider for the AI calls.

For the frontend, React was of course my choice. The premium options are backed by Stripe.

## Conclusion

You can try Airfriend by sending a WhatsApp message to +1 (628) 213-9475 or going to [its website](https://airfriend.app). It was a fun ride building it and I cannot wait to see the conversations you are going to have with it.
