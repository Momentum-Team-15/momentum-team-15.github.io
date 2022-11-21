---
layout: post
title: 🐻 File & Image Upload 🐻
tags: phase-3 phase-3-be file-upload image-upload
---

## 🗓️ Today's Topics

- How to upload files with Django
- How to configure storage for production uploads

## 🎯 Continue the Collaborative Project

Your documentation should be done and delivered to the front end by now. For an example of what your documentation should look like, see the README for the DRF Library example.

👉 If your project does not yet meet minimum requirements, you should aim for meeting them **by the end of the day Wednesday**.

## 📁 Handling requests that include attached files

#### Using Insomnia

- Select the right HTTP method for your endpoint.
- Choose binary file attachment from the body menu (where you normally put the body of a request)
- Set headers on the Headers tab (this example assumes an image file in jpeg format, named `profile-photo.jpg`):

  ```txt
  Content-Type: image/jpeg
  Content-Disposition: attachment; filename=profile-photo.jpg
  ```

For more information on the values for `Content-Type`:

- [MDN Content-Type Header](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Type)
- [MDN MIME types](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types)

#### CORS for file upload

Assuming you are using `django-cors-headers`, you'll need to add the following to `settings.py` to allow the request headers necessary for file attachments:

```py
# in settings.py

from corsheaders.defaults import default_headers

CORS_ALLOW_HEADERS = list(default_headers) + [
    'content-disposition',
]
```

## 📖 Read | 📺 Watch | 🎧 Listen

### File Upload

- [Django File (and Image) Uploads Tutorial](https://learndjango.com/tutorials/django-file-and-image-uploads-tutorial) -> A good and very recent post from Will Vincent; he does not include all the necessary info to make file uploads work in production but otherwise it's a good overview.
- 📖 [File Upload with DRF](https://goodcode.io/articles/django-rest-framework-file-upload/)
- 🎧 + 📖 [Success with Static Files](https://www.mattlayman.com/django-riffs/success-static-files/)
- 📖 [What is Amazon S3?](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html) -> Skim this -- this is Amazon's documentation and it gets really in-depth.
    - 📺 [Introduction to S3](https://www.youtube.com/watch?v=77lMCiiMilo) -> Also from Amazon

### Search

We'll cover this next week. Here is some material to get you started.

- 📖 [Basic and Full-Text Search with Django and Postgres](https://testdriven.io/blog/django-search/)
- 📖 [If you want A LOT more detail about full-text search in Postgres and Django, this blog piece has you covered](https://pganalyze.com/blog/full-text-search-django-postgres)
- 📖 [Blog post with more on full-text search](https://www.netlandish.com/blog/2020/06/22/full-text-search-django-postgresql/)
- 📺 [Search from the Ground Up](https://www.youtube.com/watch?v=is3R8d420D4&list=PL2NFhrDSOxgXXUMIGOs8lNe2B-f4pXOX-&index=2) -> Will Vincent talk at DjangoCon 2019 explaining search in detail
- 📺 [Pretty Printed: How to Perform Full Text Searches in Django with Postgres](https://www.youtube.com/watch?app=desktop&v=139a0fm0YFY)

## 🔖 Resources

### File uploads

- [Django Docs: ImageField](https://docs.djangoproject.com/en/3.2/ref/models/fields/#imagefield)
- [Django Docs: FileField](https://docs.djangoproject.com/en/3.2/ref/models/fields/#filefield)
- [Pillow: Python Imaging Library](https://pillow.readthedocs.io/en/stable/)
    - [`django-imagekit`](https://django-imagekit.readthedocs.io/en/latest/) -> If you want to resize images when they are uploaded, or do any kind of image processing, you will need this. Don't add it unless you know you need it.
- [How to Set Up Amazon S3](https://simpleisbetterthancomplex.com/tutorial/2017/08/01/how-to-setup-amazon-s3-in-a-django-project.html)
    - [AWS S3 Free Tier Info](https://aws.amazon.com/free/?all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=categories%23storage)
- [`django-storages`](https://django-storages.readthedocs.io/en/latest/index.html)
- [DRF `FileUploadParser`](https://www.django-rest-framework.org/api-guide/parsers/#fileuploadparser) _Without this you will get errors about unsupported media types_


### `@action` decorator in ViewSets

- [DRF Docs: Marking extra actions for routing with the `@action` decorator](https://www.django-rest-framework.org/api-guide/viewsets/#marking-extra-actions-for-routing)
- [DRF Docs: Routing for extra actions](https://www.django-rest-framework.org/api-guide/routers/#routing-for-extra-actions)


## 👾 Code & Notes

- [Example DRF Library API](https://github.com/Momentum-Team-15/example-drf-library-api)
