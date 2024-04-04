## CSS

### ***What is CSS?

CSS stands for Cascading Style Sheets. It is a style sheet language used for describing the visual presentation and visual formatting of a document written in markup languages like HTML and XML. CSS allows web developers to control the layout, design, colors, fonts, and other visual aspects of web pages. 

### *****What do you understand by the universal sector?**

A universal selector is a selector that used to select and apply styles to all elements within an HTML document. 

Example:

<style>

- *{

color: blue;

font-size: 10px;

}

</style>

### *****What are the elements of the CSS Box Model?**

The [CSS box model](https://www.simplilearn.com/tutorials/css-tutorial/css-box-model) defines the layout and design of CSS elements. The elements are content (like text and images), padding (the area around content), border (the area around padding), and margin (the area around the border).

### *****What is the difference between a class and an ID?**

Ans. Class is a way of using HTML elements for styling. They are not unique and have multiple elements. Whereas ID is unique and it can be assigned to a single element.

1. **Usage:**
    - **Class:** Classes can be used multiple times within the same document. They are used to style multiple elements that share similar characteristics.
    - **ID:** IDs are unique identifiers for elements. Each ID within an HTML document should be unique and used only once. IDs are typically used to uniquely style a specific element.
2. **Syntax:**
    - **Class:** In HTML and CSS, classes are denoted by a period (**`.`**) followed by the class name (e.g., **`.my-class`**).
    - **ID:** IDs are denoted by a hash/pound symbol (**`#`**) followed by the ID name (e.g., **`#my-id`**).

# **Intermediate CSS Interview Questions**

In the next section, let us learn some intermediate level CSS interview questions!

### **1. Define z-index.**

***The **`z-index`** property in CSS determines the **stacking order of elements** along the z-axis, controlling which elements appear in front or behind when they overlap. Elements with higher **`z-index`** values appear in front of elements with lower values, creating a layered effect in the webpage's layout.

### *****Explain responsive web design.**

Responsive web design is an approach to creating websites that adapt and adjust their layout, content, and design to fit various screen sizes and devices. It ensures that a website looks and functions well on desktops, laptops, tablets, and smartphones, providing an optimal viewing and user experience regardless of the device used.

### *****What is VH/VW (viewport height/ viewport width) in CSS?**

**VH and VW are CSS units used to measure viewport height and viewport width respectively in percentage form in the responsive design techniques.**

In CSS, **`vh`** (viewport height) and **`vw`** (viewport width) are relative length units that represent percentages of the viewport's height and width, respectively.

- **Viewport Height (`vh`):** 1 **`vh`** is equal to 1% of the viewport's height. For instance, if a container has a property of **`height: 50vh`**, it will take up 50% of the viewport's height, regardless of the device's screen size.
- **Viewport Width (`vw`):** 1 **`vw`** is equal to 1% of the viewport's width. Using **`width: 25vw`** for an element means it will occupy 25% of the viewport's width.

### **What is the difference between inline, inline-block, and block?**

1. **Inline:**
    - **Behavior:** Elements with **`display: inline`** do not start on a new line. They flow within the content and only take up as much width as necessary. Inline elements do not allow width or height properties to be applied.
    - **Examples:** **`<span>`**, **`<a>`**, **`<strong>`**, **`<em>`**, and other text-level elements are typically displayed inline by default.
2. **Block:**
    - **Behavior:** Elements with **`display: block`** start on a new line and occupy the full width available. They have width, height, padding, margin, and can include other block or inline elements inside them.
    - **Examples:** **`<div>`**, **`<p>`**, **`<h1>`****`<h6>`**, **`<ul>`**, **`<li>`**, **`<section>`**, and most structural elements are displayed as blocks by default.
3. **Inline-Block:**
    - **Behavior:** Elements with **`display: inline-block`** combine features of both inline and block elements. They flow within the content like inline elements but also allow for the setting of width, height, padding, margin, and other box-model properties similar to block elements.

### ***** Is it important to test the webpage in different browsers?**

Yes, it's important to test webpages in different browsers.

Different web browsers (e.g., Chrome, Firefox, Safari, Edge, etc.) can interpret and render HTML, CSS, and JavaScript differently. Testing your webpage across various browsers helps ensure consistent functionality, appearance, and user experience for all visitors regardless of the browser they use.

### ***** How is the border-box different from the content box?**

Border-box consists of properties such as content, padding, and the border with respect to height and width. However, Content-box is a default value property used for the box-sizing as well as it helps to add border and padding to give proper height and width to the box without having a border and padding properties.

### ***** Difference between CSS grid vs flexbox?**

Flexbox is designed for one-dimensional layouts, either in a row or a column. Flexbox handling the layout of individual components. It supports properties like **`justify-content`**, **`align-items`**, **`flex-direction`**, **`flex-wrap`**, etc.

CSS Grid is designed for two-dimensional layouts, allowing you to define both rows and columns. Grid managing the overall structure of the page. It supports properties like **`grid-template-columns`**, **`grid-template-rows`**, **`grid-column`**, **`grid-row`**, **`grid-gap`**, etc.

### ***** Tell us about CSS float property.**

allows other element to flow around it.

The CSS **`float`** property is used to specify how an element should float within its containing element. When you apply the float property to an element, it moves to the left or right side of its container, allowing other elements to flow around it. This property is commonly used for creating layouts where elements can be positioned side by side, such as in a multi-column layout or for positioning images within text.

***** What is CSS Box Model?**

The CSS Box Model is a fundamental concept in web design and layout. It describes the structure of every element on a web page as a rectangular box, consisting of content, padding, border, and margin.

The following figure illustrates the box model.

- **Border Area:** It is the area between the box’s padding and margin. Its dimensions are given by the width and height of the border.

border : transparent 

border :: hover : bg-blue-400

- **Margin Area:** This area consists of space between border and margin. The dimensions of the Margin area are the margin-box width and the margin-box height. It is useful to separate the element from its neighbors.
- **Padding Area:** It includes the element’s padding. This area is actually the space around the content area and within the border box. Its dimensions are given by the width of the padding-box and the height of the padding-box.
- **Content Area:** This area consists of content like text, images, or other media content. It is bounded by the content edge and its dimensions are given by content box width and height.

### *****  What are the various positioning properties in CSS?**

The *position* property in CSS tells about the method of positioning for an element or an HTML entity. There are five different types of position properties available in CSS:

1. Fixed
2. Static
3. Relative
4. Absolute
5. Sticky

Let’s talk about each of these position methods in detail:

**1. Fixed:** Any HTML element with **position: fixed** property will be positioned relative to the viewport. An element with fixed positioning allows it to remain at the same position even as we scroll the page. We can set the position of the element using the top, right, bottom, and left.

**2. Static:** This method of positioning is set by default. If we don’t mention the method of positioning for any element, the element has the **position: static** method by default. By defining Static, the top, right, bottom and left will not have any control over the element. The element will be positioned with the normal flow of the page.

**3. Relative:** An element with **position: relative** is positioned relatively with the other elements which are sitting at top of it. If we set its top, right, bottom, or left, other elements will not fill up the gap left by this element.

**4. Absolute:** An element with **position: absolute** will be positioned with respect to its parent. The positioning of this element does not depend upon its siblings or the elements which are at the same level.

**5. Sticky:** Element with **position: sticky** and **top: 0** played a role between **fixed & relative** based on the position where it is placed. If the element is placed in the middle of the document then when the user scrolls the document, the sticky element starts scrolling until it touches the top. When it touches the top, it will be fixed at that place in spite of further scrolling. We can stick the element at the bottom, with the **bottom** property.

### **[28. What is CSS overflow?](https://www.geeksforgeeks.org/css-overflow/)**

The CSS overflow controls the big content. It tells whether to clip content or to add scroll bars. The overflow contains the following property:

- visible
- hidden
- scroll
- auto

**1. Visible:** The content is not clipped and is visible outside the element box.

**2. Hidden:** The overflow is clipped and the rest of the content is invisible.

**3. Scroll:** The overflow is clipped but a scrollbar is added to see the rest of the content. The scrollbar can be horizontal or vertical.

**4. Auto:** It automatically adds a scrollbar whenever it is required.

**Overflow-x and Overflow-y:** This property specifies how to change the overflow of elements. x deals with horizontal edges and y deals with vertical edges.
