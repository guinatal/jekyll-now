---
layout: post
title: What is a WebHook?
---

A few days ago I needed to consume a webhook and it caused some confusions in my mind. Now it’s clear for me but at that time, I couldn’t understand what exacly it was, how it worked and the difference between a webservice and a webhook.

And that’s why I am here now writting this post (:

![Webhook]({{ site.url }}/images/posts/webhook.png)

## Definition

Webhooks are “user-defined HTTP callbacks”. They are usually triggered by some event, such as pushing code to a repository or a comment being posted to a blog. When that event occurs, the source site makes an HTTP request to the URI configured for the webhook. Users can configure them to cause events on one site to invoke behaviour on another. The action taken may be anything. https://en.wikipedia.org/wiki/Webhook

## Webhook vs webservice

It’s like an inverted API endpoint. Instead of making a call for any API, you define a callback URL to which the service that provide the webhook will send an HTTP POST for your API. That’s the difference between the webhook and webservice.

## Consuming a Webhook

The first thing you need to do is to set up a URL to your webhook provider. Generally, you can do it through a control panel or an API. Basically, that’s all . After a registered URL, the events will be sent to you. So now, you need to be prepared to receive them!

Below we can see a list of events and their flow. According to these events you can start creating your API.

![Sendgrid Example]({{ site.url }}/images/posts/sendgrid-webhook1.png)

![Sendgrid Example]({{ site.url }}/images/posts/sendgrid-webhook2.png)

https://sendgrid.com/docs/API_Reference/Webhooks/event.html

## Data sent

When and what kind of data will the provider send me?

It depends on your provider. Probably there is a documentation listing the events and the kind of data you need to expect. Most of webhooks will POST data to you in one of two ways: as JSON or XML to be interpreted, or as a form data (application/x-www-form-urlencoded or multipart/form-data).

Example of data:

![Sendgrid Example]({{ site.url }}/images/posts/sendgrid-webhook3.png)

https://sendgrid.com/docs/API_Reference/Webhooks/event.html

## Conclusion

Webhooks are excellent and provide us a better real time integration. It’s growing and most of the big companies already have it. Sure, you can create a webhook and not just consume them. This post was just an introduction but there are other important things, for example how to debug it and security things. You can find these kind of things easily (: