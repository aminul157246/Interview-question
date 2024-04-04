# Interview-question
## HTML

### **Basic HTML Interview Questions and Answers:**

### **1. What is HTML?**

HTML stands for Hypertext Markup Language. It's the standard markup language used in creating and designing web pages and applications. HTML provides a structure and framework for web content by using various tags to define different elements within a webpage, such as headings, paragraphs, links, images, tables, and more.

### **2. What are HTML tags?**

In HTML (Hypertext Markup Language), tags are used to **define the structure and elements** within a web page. HTML tags are composed of angle brackets **`< >`** containing the tag name, and they usually come in pairs – an opening tag and a closing tag – which enclose the content.

The basic structure of an HTML tag is:

- Opening tag: **`<tagname>`**
- Closing tag: **`</tagname>`**

### **3. What is an element in HTML?**

An element in HTML is a set of tags that define a specific part of a web page. It consists of a start tag, content, and an end tag.

### **4. What are HTML Attributes?**

HTML attributes are additional properties that provide extra information about an HTML element. These attributes are specified within the opening tag of an HTML element and are used to modify the element's behavior or provide supplementary details about it.

Attributes contain two parts: the attribute name and its value, separated by an equals sign (**`=`**) and enclosed within double quotes. For instance:

Here's an example using the **`href`** attribute within an anchor (**`<a>`**) tag:

```html

<a href="https://www.e xample.com">Click here</a>
```

### *** 5**. What is a marquee in HTML?**

Marquee is used for scrolling content on a web page. It scrolls the image or text up, down, left, or right automatically. To apply for a marquee, you have to use </marquee> tags.

### ***6. **HTML hierarchy: What is it?**

Hierarchy in HTML means how elements are organized inside other elements. This shows a parent-child relationship. For example : 

- **`<html>`** is the root element.
- **`<head>`** and **`<body>`** are child elements of **`<html>`**.
- **`<title>`** is a child of **`<head>`**.
- **`<header>`**, **`<main>`**, and **`<footer>`** are child elements of **`<body>`**.
- **`<h1>`**, **`<nav>`**, **`<ul>`**, **`<li>`**, **`<a>`**, **`<article>`**, **`<h2>`**, and **`<p>`** are all nested within their respective parent elements.

### 7.   **What is the difference between link tag <link> and anchor tag <a>?**

The **`<link>`** tag is used to link external resources to an HTML document, such as stylesheets, scripts, or other documents.

- The **`<a>`** tag is used to create hyperlinks that allow users to navigate from one webpage to another or to different sections within the same webpage.
- It is used in conjunction with the **`href`** attribute, which specifies the URL of the destination page

### 8. What are Semantic Elements?

Semantic elements = elements with a meaning.

Semantic HTML tags are tags that **define the meaning of the content they contain.**

For example, tags like **<header>**, **<article>**, and **<footer>** are semantic HTML tags. They clearly indicate the role of the content they contain.

On the other hand, tags like **<div>** and **<span>** are typical examples of non-semantic HTML elements because they serve only as content holders but give no indication.

### 9**. What is <meta> tag in HTML?**

the **`<meta>`** tag is used to provide metadata about the HTML document. Metadata is data about the HTML document itself, such as its character encoding, author, description, keywords, and viewport settings.

The **`<meta>`** tag in HTML is used to provide extra information about the webpage. This information isn't visible on the webpage itself but helps browsers and search engines understand the page better.

### 10. **What is the difference between the ‘id' and ‘class' attributes of HTML elements?**

The ‘id' attribute defines a unique identifier for an HTML element, while the ‘class' attribute defines a class for a group of elements. An ‘id' can only be used once on a page, while a ‘class' can be used multiple times.

### 11. Block-level Elements and inline element:

A block-level element always starts on a new line, and the browsers automatically add some space before and after the element. Example : `<p>` and `<div>`

An inline element does not start on a new line. Example: <span></span>
