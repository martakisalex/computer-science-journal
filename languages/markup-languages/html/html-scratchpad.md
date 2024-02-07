# HTML Scratchpad

## Understanding index.html

The `index.html` file is commonly used as the main or default webpage of a directory or website. When a web server receives a request to serve a directory and not a specific file, it typically looks for and serves the `index.html` file located within that directory.

This convention allows web developers to specify the entry point of a website or a particular section of a website. When visitors navigate to a website without specifying a particular file (for example, navigating to `http://example.com/` rather than `http://example.com/page.html`), the web server will automatically serve the `index.html` file by default.

The `index.html` file typically contains the HTML structure of the site's homepage or main landing page. It sets the tone for the website's content, design, and navigation structure.


## HTML elements

An HTML element is **anything** from the start tag to the end tag

Some HTML elements can have no content like: `<br>`

The `<html>` element is the root element and it defines the whole HTML document.

The `<body>` element defines the document's body.

While some  HTML elements will display correctly, you should **never** skip the end tag.

HTML is **not** case sensitive. However, it is common practice for tags to be lowercase.

## HTML Attributes
- All HTML elements can have attributes
- Attributes provide additional information about elements
- Attributes are always specified in the start tag
- Attributes usually come in name/value pairs like: name="value"

## HTML div

The `<div>` element is used as a container for other HTML elements.

The `<div>` element is by default a block element, meaning that it takes all available width, and comes with line breaks before and after.

If you have a `<div>` element that is not 100% wide, and you want to center-align it, set the CSS margin property to auto.

The `<div>` element has no required attributes, but `style`, `class` and `id` are common.

`<div>` as a container: The `<div>` element is often used to group sections of a web page together.
```html
<div>
  <h2>London</h2>
  <p>London is the capital city of England.</p>
  <p>London has over 13 million inhabitants.</p>
</div>
```

Multiple `<div>` elements: You can have many `<div>` containers on the same page.
```html
<div>
  <h2>London</h2>
  <p>London is the capital city of England.</p>
  <p>London has over 13 million inhabitants.</p>
</div>

<div>
  <h2>Oslo</h2>
  <p>Oslo is the capital city of Norway.</p>
  <p>Oslo has over 600.000 inhabitants.</p>
</div>

<div>
  <h2>Rome</h2>
  <p>Rome is the capital city of Italy.</p>
  <p>Rome has almost 3 million inhabitants.</p>
</div>
```

There are different methods for aligning elements side by side, all include some CSS styling. We will look at the most common methods:

**Float**: The CSS float property was not originally meant to align `<div>` elements side-by-side, but has been used for this purpose for many years.

The CSS float property is used for positioning and formatting content and allow elements float next to each other instead of on top of each other.
```html
<style>
.mycontainer {
  width:100%;
  overflow:auto;
}
.mycontainer div {
  width:33%;
  float:left;
}
</style>
```

**Inline-block**: If you change the `<div>` element's display property from block to inline-block, the `<div>` elements will no longer add a line break before and after, and will be displayed side by side instead of on top of each other.
```html
<style>
div {
  width: 30%;
  display: inline-block;
}
</style>
```

**Flex**: The CSS Flexbox Layout Module was introduced to make it easier to design flexible responsive layout structure without using float or positioning.

To make the CSS flex method work, surround the <div> elements with another <div> element and give it the status as a flex container.

## HTML Classes

The HTML class attribute is used to specify a class for an HTML element.

Multiple HTML elements can share the same class.

The `class` attribute can be used on any HTML element.

The class name is case sensitive!

The class attribute is often used to point to a class name in a style sheet.

The class attribute can also be used by JavaScript to access and manipulate elements with a specific class name.

HTML elements can belong to more than one class. You still have a single `class` attribute. However, you can have multiple class names within the attribute that are separated by spaces.
```html
<h1 class="classNameOne classNameTwo">My Title</h1>
```

Different HTML elements can point to the same class name.

The class name can also be used by JavaScript to perform certain tasks for specific elements.
JavaScript can access elements with a specific class name with the `getElementsByClassName()` method:
```javascript
function myFunction(){
    var x = getElementsByClassName();

    for(var i = 0, i < x.len(), i++){
        x[i].style.display = "none";
    }
}
```

## HTML id

The HTML `id` attribute is used to specify a unique id for an HTML element.

You cannot have more than one element with the same id in an HTML document.

The id attribute is used by CSS and JavaScript to style/select a specific element.

The value of the id attribute **must** be unique within the HTML document.

The id name is case sensitive!

The id name **must** contain at least one character, **cannot** start with a number, and **must** not contain whitespaces (spaces, tabs, etc.).

Difference Between Class and ID: A class name can be used by multiple HTML elements, while an id name must only be used by one HTML element within the page.

The id attribute is also used to create HTML bookmarks:
```html
<h2 id="C4">Chapter 4</h2>
```
Then, add a link to the bookmark ("Jump to Chapter 4"), from within the same page:
```html
<a href="#C4">Jump to Chapter 4</a>
```
Or, add a link to the bookmark ("Jump to Chapter 4"), from another page:
```html
<a href="html_demo.html#C4">Jump to Chapter 4</a>
```

The `id` attribute can also be used by JavaScript to perform some tasks for that specific element.

JavaScript can access an element with a specific id with the `getElementById()` method:
```javascript
function displayResult() {
  document.getElementById("myHeader").innerHTML = "Have a nice day!";
}
```

## Misc.
You should always include the `lang` attribute inside the `<html>` tag, to declare the language of the Web page. This is meant to assist search engines and browsers.

Country codes can also be added to the language code in the `lang` attribute. So, the first two characters define the language of the HTML page, and the last two characters define the country.

```html
<html lang="en-US">
```