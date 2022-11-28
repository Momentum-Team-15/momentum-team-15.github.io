---
layout: post
title: 🦊 File & Image Uploads 🦊
tags: phase-3 phase-3-fe
---

## 🗓️ Today's Topics

- Project progress check-in
- Get past any blockers you have

## Handling Uploaded Files

Today the back-end is learning how to accept requests that included attached files (including image files). They will need to have this implemented before you can implement it on the client side, but I'm including information here about how it's done so that you have it for reference this week.

The HTTP method for the request is dependent on how the backend implements the endpoint. The example below is an update to an existing record; notice that we are using the PATCH method. This request includes only the file itself and no JSON; notice that the file is in the second position as an argument to `axios.patch()` as the body of the request. We are also setting specific headers required by the server to handle the binary file attachment, in addition to the Authorization header.

```js
axios.patch(url, file, {
  headers: {
    Authorization: 'Token ' + token,
    'Content-Type': file.type,
    'Content-Disposition': `attachment; filename=${file.name}`
  }
}).then(res => console.log(res.data))
```

NOTE: If you Google how to include a file attachment in an AJAX request, you'll see a lot of references to [using the FormData object](https://developer.mozilla.org/en-US/docs/Web/API/FormData/Using_FormData_Objects). If you want to do it this way, please discuss with your back end devs, as they will need to make sure that they can parse MultiPart form content.

The above method does not use the FormData object. It's a little simpler in that it sends just the file and no additional data. You'll need a way to [access the file that is being uploaded by the user](https://developer.mozilla.org/en-US/docs/Web/API/File_API/Using_files_from_web_applications#accessing_selected_files). That file is what is stored in the `file` variable in the above example.

See the resources below for more information about using a file input element and accessing a selected file. [The `useRef()` hook](https://reactjs.org/docs/hooks-reference.html#useref) will be helpful to get the files from the input element after a user has selected a file using the form.

## 🔖 Resources

- [Generate random images from Unsplash without an API](https://awik.io/generate-random-images-unsplash-without-using-api/)
- [Uncontrolled components](https://reactjs.org/docs/uncontrolled-components.html)
- [Refs and the DOM](https://reactjs.org/docs/refs-and-the-dom.html) - class-based component examples
- [useRef hook](https://reactjs.org/docs/hooks-reference.html#useref)
- [MDN: File input type](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/file)
- [MDN: Accessing selected files](https://developer.mozilla.org/en-US/docs/Web/API/File/Using_files_from_web_applications#accessing_selected_files)
- [Custom hook recipes](https://usehooks.com/)
- [More custom hooks](https://github.com/streamich/react-use)
- [Official React docs on custom hooks](https://reactjs.org/docs/hooks-custom.html)
