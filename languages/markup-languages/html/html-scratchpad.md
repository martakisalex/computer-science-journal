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

## Misc.
You should always include the `lang` attribute inside the `<html>` tag, to declare the language of the Web page. This is meant to assist search engines and browsers.

Country codes can also be added to the language code in the `lang` attribute. So, the first two characters define the language of the HTML page, and the last two characters define the country.

```html
<html lang="en-US">
```