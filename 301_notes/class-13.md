# Update/Delete | Sending Form Data

**Resources:**

1. [Forms in HTML5](https://htmlreference.io/forms/)
2. [Sending form data | MDN](https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data)

## On the client side: defining how to send the data

The `<form>` element defines how the data will be sent. All of its attributes are designed to let us configure the request to be sent when a user hits a submit button. The two most important attributes are `action` and `method`.

### The action attribute

The **action attribute** defines where the data gets sent. _Its value must be a valid relative or absolute URL._ If this attribute isn't provided, the data will be sent to the URL of the page containing the form — the current page.

```html 
<!-- the data is sent to an absolute URL  -->

<form action="https://example.com">

<!-- relative URL — the data is sent to a different URL on the same origin -->
<form action="/somewhere_else">
``` 

- The names and values of the non-file form controls are sent to the server as name=value pairs joined with ampersands. 
- The action value should be a file on the server that can handle the incoming data, including ensuring server-side validation. 
- The server then responds, generally handling the data and loading the URL defined by the action attribute, causing a new page load (or a refresh of the existing page, if the action points to the same page).

## The method attribute

The `method` attribute defines how data is sent. The HTTP protocol provides several ways to perform a request; HTML form data can be transmitted via a number of different methods, the most common being the `GET method` and the `POST method`.

1. **The GET method**
    - used by the browser to ask the server to send back a given resource.
    - if a form is sent using this method the data sent to the server is appended to the URL.
2. **The POST method**
    - method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request
    - if a form is sent using this method, the data is appended to the body of the HTTP request


## Forms in HTML5

**Button Attributes:**

1. `name = "submit_button"`
    - Defines the unique identifier for that button within the form. It allows the server to access each button's value when submitted.
    - Must be unique within the context of a `<form>` container.
2. `value = "primary"`
    - The value sent to the server when submitting the form.
    - Must be unique within the context of a `<form>` container.
3. `type = "submit"` / `type = "reset"`
    - Defines the button type.
    - The button sends the form data to the server. / The button resets the form.
4. `disabled`
    - Disables the button.
5. `autofocus`
    - Sets focus on the element when the web page loads.

**Form Attributes:**

1. `action = "/contact"` / `action = "https://htmlreference.io/contact"` 
    - Defines which URL the form's information is sent to when submitted.
    - Relative URL / Absolute URL.
2. `method="post"` / `method="get"`
    - Defines the HTTP method used when submitting the form.
    - `post` - The form information is sent to the server as part of the request body.
    - `get` - The form information is sent to the server as part URL parameters
3. `name="sign_up_form"`
    - The form's name when sent to the server. Useful when multiple forms are present on the same web page.Defines the button type.
    - The name value must be unique within the context of the whole web page.
4. `autocomplete = 'off'` / `autocomplete="on"`
    - Determines if the browser can autocomplete all the form's controls.
5. `target="_blank"` / `target="_self"` / `target="_parent"` / `target="_top"`
    - Opens in : a new browsing context (new tab) / the current tab / the parent browsing context / the top browsing contex
6. `enctype="application/x-www-form-urlencoded"` / `enctype="text/plain"` / `enctype="multipart/form-data"`
    - Defines the MIME type of the information sent to the server. Only works if the method is **post**.
