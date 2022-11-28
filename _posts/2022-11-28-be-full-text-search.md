---
layout: post
title: 🐻 Postgres Full-Text Search 🐻
tags: phase-3 phase-3-be full-text-search
---

## Today's Topics

- Checking in on project progress 👀
- Implementing search, including Postgres full-text search

## 🎯 Project due on Thursday afternoon

**Please include a README** in your project repo. The README should:

- be written in Markdown
- include a link to your production application
- have instructions for getting your application running locally, so that any developer could pull it down and run it.

**Your README must include documentation for your API's available endpoints.**

👉 If your project meets minimum requirements today, HUZZAH! That is awesome. You should be working on **at least one additional or spicy feature**.

👉 If your project does not yet meet minimum requirements, your goal should be meeting them **by the end of the day Wednesday**.

### Note

Depending on how you've constructed your API, you might have separate endpoints for all of the below, or you might have fewer endpoints (for instance, if you nested answers in the question detail endpoint, like `questions/4/answers`). What matters is that you have endpoints that your front-end team can use to perform all the necessary actions they need and that are documented in your README.

### Minimum Requirements for QuestionBox, Back End

⚠️ Be sure to test that you have implemented permissions-checking correctly for these endpoints. For example, your API should not allow a user who is not the question-asker to mark an answer as accepted.

- token login, logout, and register (i.e., create a new user)
- list all questions
- list answers to a specific question
- show details about a specific question
- create a question
- create an answer to a question (if you are not the question owner)
- mark an answer as "accepted" (if you are the question owner)
- list of own questions for an authenticated user
- list of own answers for an authenticated user
- star/favorite questions or answers
- unstar/unfavorite questions or answers
- search questions (possibly both questions and answers)
- A README with endpoints documented

### Minimum Requirements for Social Cards, Back End

⚠️ Be sure to test that you have implemented permissions-checking correctly for these endpoints. For example, your API should not allow a user who is not the creator of a card to update a card.

- token login, logout, and register (i.e., create a new user)
- list all cards
- list all cards you've created (you, the logged in user)
- list all cards created by a user you follow
- show details of one card (with front and back messages)
- create a new card
- update a card you've made
- delete a card you've made
- follow another user
- unfollow another user
- list all the users you follow
- A README with endpoints documented

## 📖 Read | 📺 Watch | 🎧 Listen

- 📖 [Basic and Full-Text Search with Django and Postgres](https://testdriven.io/blog/django-search/)
- 📖 [If you want A LOT more detail about full-text search in Postgres and Django, this blog piece has you covered](https://pganalyze.com/blog/full-text-search-django-postgres)
- 📖 [Blog post with more on full-text search](https://www.netlandish.com/blog/2020/06/22/full-text-search-django-postgresql/)
- 📺 [Search from the Ground Up](https://www.youtube.com/watch?v=is3R8d420D4&list=PL2NFhrDSOxgXXUMIGOs8lNe2B-f4pXOX-&index=2) -> Will Vincent talk at DjangoCon 2019 explaining search in detail
- 📺 [Pretty Printed: How to Perform Full Text Searches in Django with Postgres](https://www.youtube.com/watch?app=desktop&v=139a0fm0YFY)
- 📺 [Full Text Search with Django and PostgreSQL: More Facets, Less Dependencies](https://youtu.be/QFs6qgvyTC4) -> Team 11 Momentum grad Jason Judkins is a co-presenter of this talk given at last month's DjangoCon! 🤩

## 🔖 Resources

### Filtering and search

- [DRF - Filtering](https://www.django-rest-framework.org/api-guide/filtering/) -> Pretty useful reference. Includes how to filter your output based on GET parameters, which you will want to do for using search terms.
- [Django Docs: full-text search & the search lookup](https://docs.djangoproject.com/en/4.0/ref/contrib/postgres/search/#the-search-lookup)
- [Django Docs: SearchVector](https://docs.djangoproject.com/en/4.0/ref/contrib/postgres/search/#searchvector) -> You'll need this if you want to search against more than a single field

### Pagination

- [DRF docs: Pagination](https://www.django-rest-framework.org/api-guide/pagination/)

## 👾 Code & Notes

- [DRF Library API](https://github.com/Momentum-Team-15/example-drf-library-api)
- [Notes on Django Queries](https://github.com/Momentum-Team-13/notes/blob/main/django-queries.md) These are the same notes you may have seen at the beginning of the Phase. I'm including them here for easy reference, as they show examples of queries and filters that might come in handy for search endpoints.
