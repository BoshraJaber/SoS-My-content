# Styling HTML `<input>` like a pro:

# Unserstand `input` element

This article will provide you with all the css properties to style your form inputs, it will not include commonly properties.

Before we dive in, few things to note about HTML input:

- By defult, input appearce are predefined by user agent (web browser) as they are replaced element, that's why by default it won't take the full width of its parent.
- similar to all replaced element in HTML, it is not possible to use psuedo elements with Input (depending on the type attribute), for example, ::before + after
- There is a simple trick to use pusedo elements:
  snippet 1:

```html
<style>
  input.use-psudo-element {
    padding-right: 30px;
  }
  input.use-psudo-element + *:before {
    content: "🔍";
    position: absolute;
    top: 0px;
    right: -30px;
  }
</style>
<section class="position-relative">
  <input
    id="searchInput"
    class="use-psudo-element"
    type="text"
    placeholder="Search ..."
  />
  <span></span>
</section>
```

Note: padding-right is used to avoid the text inside the input of overlapping with the image, uit sould be at least the same with of the image.

### Use Padding instead of Height

### pseudo-classes:

#### :in-range & :out-of-range:

```html
<style>
  input:in-range {
    background-color: palegreen;
    border: 2px solid green;
  }
  input:out-of-range {
    background-color: orangered;
    border: 2px solid red;
  }
</style>
<section class="position-relative">
  <label for="price">Price (range fron 1 - 10)</label>
  <input name="price" type="number" min="1" max="10" value="4" />
</section>
```

#### :valid & :invalid:

```html
<style>
  input:valid {
    background-color: ivory;
    border: none;
    outline: 2px solid deepskyblue;
    accent-color: gold;
  }
  input:invalid {
    background-color: orangered;
    border: 2px solid red;
    accent-color: gold;
  }
</style>
<section class="position-relative">
  <label for="email">Email Address:</label>
  <input name="email" type="email" value="na@me@example.com" />
</section>
```

#### :required:

### :focus: It is generally triggered when the user clicks or taps on an element or selects it with the keyboard's Tab key.

```html
input:focus { background-color: lightblue; }
```

#### ::placeholder psudo element & :placeholder-shown psudo class:

- placeholder: reperent the placeholder
- placeholder-shown: represent the input that has the placeholder, can still affect the styling of the placeholder text, since it’s a parent element (e.g. font-size).
- Firefox makes placeholder text of input elements semi-transparent. When setting a custom color for placeholder text, keep in mind that it will appear a bit dimmed. A way to fix that is addin opacity:1;

```css
// P.S. Do not use them all together (this selector is broken and css parser will always fails):

::-webkit-input-placeholder {
  /* Chrome/Opera/Safari */
  color: pink;
}
::-moz-placeholder {
  /* Firefox 19+ */
  color: pink;
}
:-ms-input-placeholder {
  /* IE 10+ */
  color: pink;
}
:-moz-placeholder {
  /* Firefox 18- */
  color: pink;
}
```

- Not all input are replaced element, based on type attribute, According to MDN,
  > HTML spec also says that an <input> element can be replaced, because <input> elements of the "image" type are replaced elements similar to <img>. However, other form controls, including other types of <input> elements, are explicitly listed as non-replaced elements (the spec describes their default platform-specific rendering with the term "Widgets").
  > In certain cases (typically involving non-textual inputs and specialized interfaces), the <input> element is a replaced element.

The appearance and behavior of the <input> element are determined by the user agent's default styles or any custom styles applied to it.
To answer this question, we need to understand what is a replaced element in html, which is an element that its appreance predefined by web browser without any css,

Input by defaul it takes `display: inline-block;`

```
    margin: 0em;
    padding: 1px 2px;
    border-width: 2px;
```

They can be marked as readonly (the user cannot modify the input value but it is still sent with the rest of the form data) or disabled (the input value can't be modified and is never sent with the rest of the form data).
They can have a placeholder; this is the text that appears inside the text input box that should be used to briefly describe the purpose of the box.
They can be constrained in size (the physical size of the box) and maxlength (the maximum number of characters that can be entered into the box).
They can benefit from spell checking (using the spellcheck attribute), if the browser supports it.

### Resources:

- [Challenges in styling form widget](https://developer.mozilla.org/en-US/docs/Learn/Forms/Styling_web_forms)
- [Debugging CSS by Ahmad Shadeed](https://debuggingcss.com/)
