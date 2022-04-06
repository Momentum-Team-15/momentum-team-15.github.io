---
layout: post
title: 🐻 Designing Your Models & Your API 🐻
tags: phase-3 phase-3-be django rest
---

## 🗓️ Today's Topics

- Models for your collaborative project
- Designing the urls you need
- Review permissions & CORS

## 🎯 Project

Today you should have your models nailed down and be able to work with them in the admin and the shell -- that is, you can save them to the database and retrieve them, and all the relationships work properly.

You should have a **WRITTEN DOWN** plan for at least the basic set of urls that your front-end will need. You may make changes to this as you go but you need a place to begin.

When creating your list of endpoints, remember: **only build what you need.**

- What lists or collections of data will you need to return?
- What single resources will you need to return?
- What HTTP methods will you need to support for your urls?
- Which routes will need to be authenticated and which do not require authentication?
- Will you need to restrict any actions at the object level?

### By Friday

Your API should...

- be returning JSON for GET requests for questions and answers / cards and friends
- be able to accept POST requests to create questions and answers / cards and friends

## 🔖 Resources

- [A Long (Mostly Helpful) List of Things to Keep In Mind When You're Building an API](https://betterprogramming.pub/22-best-practices-to-take-your-api-design-skills-to-the-next-level-65569b200b9) -> _Many of these best practices you get for free with DRF; some are included with packages we use; and some of this is advice for the choices you have to make in the code you write._
- [Overview of creating an API](https://www.caktusgroup.com/blog/2019/02/01/creating-api-endpoint-django-rest-framework/) -> _Nothing much new in this article, but it is a good summary and high-level overview of how to go about creating an API with DRF._
- [How to Save Extra Data to a DRF Serializer](https://simpleisbetterthancomplex.com/tutorial/2019/04/07/how-to-save-extra-data-to-a-django-rest-framework-serializer.html) -> _This is essential for adding in extra info that is not included in your serializer, like the user (from request.user) that is associated with the object you want to create._

### Permissions

- [DRF Permissions](https://testdriven.io/blog/drf-permissions/)
- [Built-in Permission Classes in DRF](https://testdriven.io/blog/built-in-permission-classes-drf/)
- [Custom Permissions in DRF](https://testdriven.io/blog/custom-permission-classes-drf/)
- [Pro-Tip: Logical operators with DRF Permissions](https://www.revsys.com/tidbits/tip-about-drf-permissions/)

### CORS

- [MDN CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
    - [MDN Access-Control-Allow-Origin Header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Origin)
- [Julia Evans comic explaining CORS better than MDN does](https://twitter.com/b0rk/status/1162392625057583104?lang=en)
- [Django CORS Guide](https://www.stackhawk.com/blog/django-cors-guide/)
- [`django-cors-headers`](https://github.com/adamchainz/django-cors-headers)


## 🦉 Code

- [Example Library API](https://github.com/Momentum-Team-11/example-drf-library)
