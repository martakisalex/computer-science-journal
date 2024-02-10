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

## Anatomy of an HTML element

![Anatomy of an HTML element](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started/grumpy-cat-small.png)
The anatomy of our element is:

**The opening tag**: This consists of the name of the element (in this example, p for paragraph), wrapped in opening and closing angle brackets. This opening tag marks where the element begins or starts to take effect. In this example, it precedes the start of the paragraph text.

**The content**: This is the content of the element. In this example, it is the paragraph text.

**The closing tag**: This is the same as the opening tag, except that it includes a forward slash before the element name. This marks where the element ends. Failing to include a closing tag is a common beginner error that can produce peculiar results.

The element is the opening tag, followed by content, followed by the closing tag.

## Nesting elements

Elements can be placed within other elements. This is called nesting. If we wanted to state that our cat is **very** grumpy, we could wrap the word very in a `<strong>` element, which means that the word is to have strong(er) text formatting:
```html
<p>My cat is <strong>very</strong> grumpy.</p>
```
The tags have to open and close in a way that they are inside or outside one another.

## Void Elements

Not all elements follow the pattern of an opening tag, content, and a closing tag. Some elements consist of a single tag, which is typically used to insert/embed something in the document. Such elements are called void elements. For example, the `<img>` element embeds an image file onto a page:
```html
<img
  src="https://raw.githubusercontent.com/mdn/beginner-html-site/gh-pages/images/firefox-icon.png"
  alt="Firefox icon" />
```

## HTML Attributes

- All HTML elements can have attributes
- Attributes provide additional information about elements
- Attributes are always specified in the start tag
- Attributes usually come in name/value pairs like: name="value"

Attributes contain extra information about the element that won't appear in the content.

### Boolean Attributes

*Sometimes you will see attributes written without values*. This is entirely acceptable. These are called Boolean attributes.
```html
<input type="text" disabled="disabled" />
```
As shorthand, it is acceptable to write this as follows:
```html
<input type="text" disabled />
```

#### Good example of incorrect syntax

```html
<a href=https://www.mozilla.org/ title=The Mozilla homepage>favorite website</a>
```
As written above, the browser misinterprets the markup, mistaking the `title` attribute for three attributes: a title attribute with the value `The`, and two Boolean attributes, `Mozilla` and `homepage`.

Always include the attribute quotes. It avoids such problems, and results in more readable code.

## Anatomy of an HTML document

```html
<!DOCTYPE html>
<html lang="en-US">
  <head>
    <meta charset="utf-8" />
    <title>My test page</title>
  </head>

  <body>
    <p>This is my page</p>
  </body>
</html>
```

### `<!DOCTYPE html>`

The doctype. When HTML was young (1991-1992), doctypes were meant to act as links to a set of rules that the HTML page had to follow to be considered good HTML. Doctypes used to look something like this: 
```html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```
More recently, the doctype is a historical artifact that needs to be included for everything else to work right. `<!DOCTYPE html>` is the shortest string of characters that counts as a valid doctype. That is all you need to know!

### `<html></html>`

The `<html>` element. This element wraps all the content on the page. It is sometimes known as the root element.

### `<head></head>`

The `<head>` element. This element acts as a container for everything you want to include on the HTML page, that isn't the content the page will show to viewers. This includes keywords and a page description that would appear in search results, CSS to style content, character set declarations, and more. You will learn more about this in the next article of the series.

### `<meta charset="utf-8">`

The `<meta>` element. This element represents metadata that cannot be represented by other HTML meta-related elements, like `<base>`, `<link>`, `<script>`, `<style>` or `<title>`. The charset attribute specifies the character encoding for your document as UTF-8, which includes most characters from the vast majority of human written languages. With this setting, the page can now handle any textual content it might contain. There is no reason not to set this, and it can help avoid some problems later.

### `<title></title>`

The `<title>` element. This sets the title of the page, which is the title that appears in the browser tab the page is loaded in. The page title is also used to describe the page when it is bookmarked.

### `<body></body>`

The `<body>` element. This contains all the content that displays on the page, including text, images, videos, games, playable audio tracks, or whatever else.

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