---
layout: post
title: 🐻 Token Authentication and CORS 🐻
tags: phase-3 phase-3-be djoser token-auth cors
---

## 🗓️ Today's Topics

- API project review
- Follow up on yesterday's project planning
- Token authentication in DRF with Djoser
- CORS headers
- Git Workflow

## 🎯 Collaborative Project

Work with your team. Today you should be writing code for your **models** referring to the diagram you made. Be sure to test out your models in the Django shell and/or admin to see if they work the way you intend. Once you have models in place you can begin work on endpoints.

## 📖 Read | 📺 Watch | 🎧 Listen

- 📺 [Finally Understand Auth in DRF - a Will Vincent talk](https://www.youtube.com/watch?v=pY-oje5b5Qk) -> Will isn't using the Djoser library but he does a great job of reviewing different auth strategies and why you would choose one or the other. Watch this for a better understanding and overview of authentication.
- 📖 [Julia Evans comic explaining CORS better than MDN does](https://twitter.com/b0rk/status/1162392625057583104?lang=en)
- 📖 [More Julia Evans on the Same Origin Policy](https://twitter.com/b0rk/status/1155493682885341184)
- 📖 [A Visual Guide to CORS by Lydia Hallie](https://dev.to/lydiahallie/cs-visualized-cors-5b8h)
- 📖 [Simple Is Better Than Complex: How to Implement Token Authentication in DRF](https://simpleisbetterthancomplex.com/tutorial/2018/11/22/how-to-implement-token-authentication-using-django-rest-framework.html) _This does NOT use Djoser, but it's a great walkthrough of some of what Djoser does for you if you would like more detail._

## 🔖 Resources

### Authentication

- [Djoser documentation](https://djoser.readthedocs.io/en/latest/)
- [DRF docs: Token-based authentication](https://www.django-rest-framework.org/api-guide/authentication/#tokenauthentication)
- [The Ultimate Tutorial for Django REST Framework: Login and Authentication](https://sunscrapers.com/blog/django-rest-framework-login-and-authentication/) _This uses the Djoser library._

### CORS

- [MDN CORS](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)
    - [MDN Access-Control-Allow-Origin Header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Access-Control-Allow-Origin)
- [Django CORS Guide](https://www.stackhawk.com/blog/django-cors-guide/)
- [`django-cors-headers`](https://github.com/adamchainz/django-cors-headers)

### Permissions

- [DRF Permissions](https://www.django-rest-framework.org/api-guide/permissions/)
- [Pro-Tip: Logical operators with DRF Permissions](https://www.revsys.com/tidbits/tip-about-drf-permissions/)

## 👾 Code & Notes

- [Example DRF Library API](https://github.com/Momentum-Team-15/example-drf-library-api)
- [Git Collaboration slide deck](https://slides.com/amy_nc/git-collaboration)
