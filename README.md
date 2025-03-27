# BaseJS Documentation

**BaseJS** is a utility JavaScript library that provides a collection of generic methods for DOM manipulation, event handling, and form processing. This library is designed to be lightweight and easy to integrate into any web project.

## Methods

### `domready(fn)`

Executes a function when the DOM is fully loaded.

- **Parameters**: 
  - `fn` (Function): The function to execute when the DOM is ready.

### `uid()`

Generates a unique identifier for creating a DOM element ID.

- **Returns**: 
  - `String`: A unique identifier string.

### `exists(a)`

Checks if an object is not null and not undefined.

- **Parameters**: 
  - `a` (Any): The object to check.
- **Returns**: 
  - `Boolean`: `true` if the object exists, `false` otherwise.

### `toCamel(a)`

Converts a string to camel case.

- **Parameters**: 
  - `a` (String): The string to convert.
- **Returns**: 
  - `String`: The camel-cased string.

### `toBoolean(a)`

Converts a string to a boolean. If already a boolean, returns the boolean.

- **Parameters**: 
  - `a` (Any): The value to convert.
- **Returns**: 
  - `Boolean`: The boolean value.

### `isFunction(a)`

Verifies if an object is a function.

- **Parameters**: 
  - `a` (Any): The object to check.
- **Returns**: 
  - `Boolean`: `true` if the object is a function, `false` otherwise.

### `isNodeList(nodes)`

Checks if an object is a node list.

- **Parameters**: 
  - `nodes` (Any): The object to check.
- **Returns**: 
  - `Boolean`: `true` if the object is a node list, `false` otherwise.

### `isArray(a)`

Verifies if an object is an array.

- **Parameters**: 
  - `a` (Any): The object to check.
- **Returns**: 
  - `Boolean`: `true` if the object is an array, `false` otherwise.

### `isString(a)`

Verifies if an object is a string.

- **Parameters**: 
  - `a` (Any): The object to check.
- **Returns**: 
  - `Boolean`: `true` if the object is a string, `false` otherwise.

### `isBoolean(a)`

Verifies if an object is a boolean.

- **Parameters**: 
  - `a` (Any): The object to check.
- **Returns**: 
  - `Boolean`: `true` if the object is a boolean, `false` otherwise.

### `isElement(a)`

Verifies if an object is a DOM element.

- **Parameters**: 
  - `a` (Any): The object to check.
- **Returns**: 
  - `Boolean`: `true` if the object is a DOM element, `false` otherwise.

### `isUri(a)`

Verifies if a string is a URI.

- **Parameters**: 
  - `a` (String): The string to check.
- **Returns**: 
  - `Boolean`: `true` if the string is a URI, `false` otherwise.

### `isJson(a)`

Verifies if a string is JSON.

- **Parameters**: 
  - `a` (String): The string to check.
- **Returns**: 
  - `Boolean`: `true` if the string is JSON, `false` otherwise.

### `isInput(a)`

Determines if an element is an input or textarea control.

- **Parameters**: 
  - `a` (Any): The object to check.
- **Returns**: 
  - `Boolean`: `true` if the object is an input or textarea, `false` otherwise.

### `eventSource(a)`

Returns the DOM element that generated the event.

- **Parameters**: 
  - `a` (Event): The event object.
- **Returns**: 
  - `Element`: The source element of the event.

### `getElement(a)`

Returns the DOM element with the specified ID.

- **Parameters**: 
  - `a` (String): The ID of the element.
- **Returns**: 
  - `Element`: The DOM element with the specified ID.

### `getElementBySelector(selector, el)`

Returns the first element that matches the selector.

- **Parameters**: 
  - `selector` (String): The CSS selector.
  - `el` (Element, optional): The parent element to search within.
- **Returns**: 
  - `Element`: The first matching element.

### `getElementsBySelector(a, el)`

Returns all elements that match the selector.

- **Parameters**: 
  - `a` (String): The CSS selector.
  - `el` (Element, optional): The parent element to search within.
- **Returns**: 
  - `NodeList`: A list of matching elements.

### `getElementValue(a)`

Returns the value of the DOM element with the specified ID.

- **Parameters**: 
  - `a` (String): The ID of the element.
- **Returns**: 
  - `String`: The value of the element.

### `getElementUrl(element)`

Returns the first attribute of an element that matches a URL.

- **Parameters**: 
  - `element` (Element): The DOM element.
- **Returns**: 
  - `String`: The URL attribute value.

### `getFirstForm()`

Returns the first form element on the page.

- **Returns**: 
  - `Element`: The first form element.

### `getToken(form)`

Gets a request verification token from within a form.

- **Parameters**: 
  - `form` (Element, optional): The form element.
- **Returns**: 
  - `Element`: The request verification token element.

### `show(el, display)`

Sets the element to display:block (or override with something else) and sets opacity to 1.

- **Parameters**: 
  - `el` (Element): The element to show.
  - `display` (String, optional): The display style. Default is "block".

### `hide(el)`

Sets the element to display:none.

- **Parameters**: 
  - `el` (Element): The element to hide.

### `fadeOut(el, completeFunction, intervalSpeed)`

Fades an element out and sets display:none on it.

- **Parameters**: 
  - `el` (Element): The element to fade out.
  - `completeFunction` (Function, optional): The function to execute after fading out.
  - `intervalSpeed` (Number, optional): The speed of the fade effect. Default is 25.

### `fadeIn(el, completeFunction)`

Fades an element in.

- **Parameters**: 
  - `el` (Element): The element to fade in.
  - `completeFunction` (Function, optional): The function to execute after fading in.

### `setFieldValidations()`

Loads all field validations on a page that have an error and applies an 'is-invalid' class to the calling inputs.

### `showBusy()`

Makes a button show a busy animation and disables it.

- **Returns**: 
  - `Object`: An object containing the ID and HTML of the button.

### `showOriginal(button, busy)`

Returns a button back to the original state.

- **Parameters**: 
  - `button` (Element): The button element.
  - `busy` (Object): The result from `showBusy()` method.

### `createFormData(form)`

Creates a new instance of FormData.

- **Parameters**: 
  - `form` (Element, optional): The form element to hydrate new data.
- **Returns**: 
  - `FormData`: The FormData object.

### `getDataFromTag(element, dataTag)`

Gets a basejs attribute from a form element.

- **Parameters**: 
  - `element` (Element): The DOM element.
  - `dataTag` (String): The data tag.
- **Returns**: 
  - `String`: The attribute value.

### `clearValidationSummary(formElement)`

Clears validation summary errors inside a form element.

- **Parameters**: 
  - `formElement` (Element): The form element.

### `postForm(uri, formData, successFunction, errorFunction, completeFunction, methodType)`

Posts (or gets) a form to the specified URI with the formData.

- **Parameters**: 
  - `uri` (String): The URI to post to.
  - `formData` (FormData): The form data.
  - `successFunction` (Function, optional): The function to execute on success.
  - `errorFunction` (Function, optional): The function to execute on error.
  - `completeFunction` (Function, optional): The function to execute on completion.
  - `methodType` (String, optional): The HTTP method. Default is "POST".

Sure, I'll continue documenting from the `postAndReplace` method to the bottom of the file:

---

### `postAndReplace(ev, uri, replaceElementId, successFunction, errorFunction, completeFunction, closeModalElementId)`

Posts data to the specified URI from a form onsubmit event and replaces the data coming back with the specified element's inner HTML.

- **Parameters**: 
  - `ev` (Event): The event that triggered the post.
  - `uri` (String): The URI to post to.
  - `replaceElementId` (String): The ID of the element to replace with the response.
  - `successFunction` (Function, optional): The function to execute on success.
  - `errorFunction` (Function, optional): The function to execute on error.
  - `completeFunction` (Function, optional): The function to execute on completion.
  - `closeModalElementId` (String, optional): The ID of the modal element to close.

### `getFunctionFromString(string)`

Gets a function from a string representation.

- **Parameters**: 
  - `string` (String): The string representation of the function.
- **Returns**: 
  - `Function`: The function object.

### `initValidations()`

Initializes all validations so that once you start typing, it will clear out errors.

### `clearError(ev)`

Clears validation errors when a user starts typing into a field.

- **Parameters**: 
  - `ev` (Event): The event to use to clear the validations.

### `copyInputField(ev, sourceId, targetId)`

Copies input value from one input control to another.

- **Parameters**: 
  - `ev` (Event): The event that triggered the copy.
  - `sourceId` (String, optional): The ID of the source input element.
  - `targetId` (String, optional): The ID of the target input element.

### `autoFocus()`

Finds the first auto-focus entry and sets it as the current field.

### `initForms()`

Automatically loads forms on the page without requiring the onsubmit routine on each one.

### `initButtons()`

Automatically loads buttons to copy data from one field to another.

### `executeDeferredFunctions()`

Executes deferred functions after the DOM is ready.

### `init()`

Initializes anything on the page that is needed.
