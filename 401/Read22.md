# Django CRUD and Forms
- An HTML Form is a group of one or more fields/widgets on a web page that can be used to collect information from users as a submission to a server.
Forms are a flexible mechanism for collecting user input because there are suitable widgets for entering many different types of data, including text boxes, checkboxes, radio buttons, date pickers and so on.

- Working with forms can be complicate , Developers need to write HTML for the form, validate and properly sanitize entered data on the server (and possibly also in the browser), repost the form with error messages to inform users of any invalid fields, handle the data when it has successfully been submitted, and finally respond to the user in some way to indicate success.

- **Django Forms do a lot of the work out of all these steps** by providing a framework that lets you define forms and their fields programmatically,then use these objects to both generate the form HTML code and handle much of the validation and user interaction.

	
### HTML Forms
- The form is defined in HTML as a collection of elements inside `<form>...</form>` tags, containing at least one `input` element of `type="submit"`.

- The field's type attribute defines what sort of widget will be displayed. The name and id of the field are used to identify the field in JavaScript/CSS/HTML, while value defines the initial value for the field when it is first displayed.
- The form attributes define the HTTP method used to send the data and the destination of the data on the server (action):
- **action:** The resource/URL where data is to be sent for processing when the form is submitted. If this is not set, then the form will be submitted back to the current page URL.
- **method:** The HTTP method used to send the data: post or get.
  - The `POST` method should always be used if the data is going to result changing on the server's database because this can be made more resistant to cross-site forgery request attacks.
  - The `GET` method should only be used for forms that don't change user data (e.g. a search form). It is recommended for when you want to be able to bookmark or share the URL.

  	
### Django form handling process
- Display the default form the first time it is requested by the user.
  - The form may contain blank fields, or it may be pre-populated with initial values.
  - The form is referred to as unbound at this point, because it isn't associated with any user-entered data.
- Receive data from a submit request and bind it to the form.
  - Binding data to the form means that the user-entered data and any errors are available when we need to redisplay the form.
- Clean and validate the data.
  - Cleaning the data performs sanitization of the input and converts them into consistent Python types.
  - Validation checks that the values are appropriate for the field
- If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields.
- If all the data is valid, perform required actions
- Once all actions are complete, redirect the user to another page.