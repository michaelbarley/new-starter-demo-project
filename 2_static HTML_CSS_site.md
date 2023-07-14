# Static HTML/CSS site
By the end of this section you will have a fully functionl ecommerce landing page written in HTML & CSS! Lets do this 🚀

## 1. Folder Setup 
1. Open Finder (located usually on your dock)
2. in the finder window click on `Documents`
3. Right click (on mac, right click is sometimes disabled you may have to two-finger click on the lower right of your trackpad) and click on `New Folder`
4. Name this folder `Shoes`
5. Click into `Shoes` folder and create a new folder named `image`
6. go to https://drive.google.com/drive/folders/1VCFjiogucrQHMW24E_EqDw3L18cfJNLz?usp=share_link. Shift click all the images, then right click and download
7. once the images have donwloaded they should appear if you Navigate to `Downloads` in finder.
8. Drag and drop all those downloaded images into your `Documents/Shoes/image` directory
<img width="908" alt="Screenshot 2023-07-14 at 13 52 10" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/63ac34c0-f313-42b2-a053-0cd3faf40342">

## 2. index.html
Now lets create our first HTML file.

### What is HTML
HTML is the standard markup language for creating Web pages.
- HTML stands for Hyper Text Markup Language
- HTML is the standard markup language for creating Web pages
- HTML describes the structure of a Web page
- HTML consists of a series of elements
- HTML elements tell the browser how to display the content
- HTML elements label pieces of content such as "this is a heading", "this is a paragraph", "this is a link", etc.

1. Drag `Shoes` folder into your code editor of choice (this will open the folder up in a code editor)
2. Within your code editor (i'm using Visual Studio Code) Right click outside the `image` folder and select `new file` name this file `index.hmtl`

### Whats index.html
The file named index.html is often the first file that is loaded when a user navigates to a website. This convention originated from the early days of the internet and has stuck around due to its widespread usage and support.

Here are a few reasons why index.html is usually the first HTML file in a web project:

**Default Entry Point**: When a URL points to a directory and not a specific file (like https://www.example.com/), the web server looks for a default file to serve. This file is usually called index.html. It's like the homepage or the front door of your website.

**Convention**: It's a widely adopted convention. Most web developers, hosting services, and server configurations adhere to this practice, making it a standard across the industry. Following this convention ensures compatibility and reduces confusion.

**Ease of Use**: When the main file of a website is named index.html, other developers (or even the future version of you) can easily understand where to look for the primary HTML file. This enhances maintainability and collaboration.

In summary, naming your first HTML file as index.html makes your website accessible to users, follows industry standards, and aids in the ease of understanding your project's structure. It's important to note, however, that this can be configured differently on the server-side if needed, but doing so without a specific reason may lead to unnecessary confusion.

### A Simple HTML Document
Inside the `index.html` write:
```html
<!DOCTYPE html>
<html>

<head>
    <title>Page Title</title>
</head>

<body>

    <h1>My First Heading</h1>
    <p>My first paragraph.</p>

</body>

</html>
```

**Example Explained**
- The `<!DOCTYPE html>` declaration defines that this document is an HTML5 document
- The `<html>` element is the root element of an HTML page
- The `<head>` element contains meta information about the HTML page
- The `<title>` element specifies a title for the HTML page (which is shown in the browser's title bar or in the page's tab)
- The `<body>` element defines the document's body, and is a container for all the visible contents, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.
- The `<h1>` element defines a large heading
- The `<p>` element defines a paragraph

### What is an HTML Element?
An HTML element is defined by a start tag, some content, and an end tag:
`<tagname> Content goes here... </tagname>`

The **HTML element** is everything from the start tag to the end tag:
```html
<h1>My First Heading</h1>
<p>My first paragraph.</p>
```
<img width="846" alt="Screenshot 2023-07-14 at 14 10 55" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/cb369c56-37d8-439b-ab19-1c179ce74f54">

3. In finder double click on `index.html` and it will open it up in your defult browser. You should now see our HTML rendered in the browser! 
<img width="1317" alt="Screenshot 2023-07-14 at 14 10 31" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/8bb3f18a-06f8-469c-9d15-d36ea4258ae4">

4. Now lets update our `index.html` with a few new tags, modify `index.html` `<head>` like so: 
```html
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nike - Just Do It</title>
    <link rel="stylesheet" href="style.css">
    <link rel="shortcut icon" href="image/logo.png">
</head>
```

let's break down each of these tags:

`<meta charset="UTF-8">`: The `<meta>` tag provides metadata about the HTML document. Metadata isn't displayed on the page but is machine parsable. In this case, the charset attribute specifies the character encoding for the HTML document. UTF-8 is a universal character set that includes all characters from all writing systems, so it's good practice to use this to support international characters and symbols.

`<meta http-equiv="X-UA-Compatible" content="IE=edge">`: This `<meta>` tag is used for compatibility with Internet Explorer. It tells IE to display the webpage in the highest mode available, thus ensuring the webpage uses the latest rendering engine. edge means the very latest version that IE has to offer.

`<meta name="viewport" content="width=device-width, initial-scale=1.0">`: This `<meta>` tag is used for responsive web design. It sets the width of the page to follow the screen-width of the device (which will vary depending on the device). The initial-scale=1.0 part sets the initial zoom level when the page is first loaded by the browser.

`<link rel="stylesheet" href="style.css">`: The `<link>` tag defines the relationship between the current document and an external resource. In this case, it's linking to an external CSS file (style.css) which provides the styles for the HTML document. The rel attribute specifies the relationship as a "stylesheet".

`<link rel="shortcut icon" href="image/logo.png">`: This `<link>` tag is used to specify a shortcut icon or favicon for the HTML document. The favicon is a small icon that appears in the browser tab next to the webpage's title. The href attribute specifies the path to the image file.

### Navigation Bar
5. Within our `<body>` place this code: 
```html
    <section>
        <nav>
            <div class="logo">
                <h1>Shoe<span>s</span></h1>
            </div>

            <ul>
                <li><a href="#Home">Home</a></li>
                <li><a href="#Products">Products</a></li>
                <li><a href="#About">About</a></li>
                <li><a href="#Review">Review</a></li>
                <li><a href="#Servises">Servises</a></li>
            </ul>
        </nav>
    </section>
```

let's break down each of these tags:

`<section>`: The `<section>` tag defines sections in a document, such as chapters, headers, footers, or any other sections of the document.
  
`<nav>`: The `<nav>` tag defines a set of navigation links. Using this tag helps search engines understand the structure of the website. It is intended for major block of navigation links, not for scattered links within the page.

`<div class="logo">`: The `<div>` tag is used as a container that divides an HTML document into sections. It can be styled with CSS (Cascading Style Sheets) or manipulated with JavaScript. In this case, it's used to contain the logo of the page. The class attribute is used to point to a class name in a style sheet.

`<h1>Shoe<span>s</span></h1>`: The `<h1>` tag is used to indicate the main heading of a page, and should be the title of the whole content. The <span> tag is used to group inline-elements in a document. Here, it's used to separate the "s" in "Shoes" for potential styling purposes.

`<ul>`: The `<ul>` tag stands for Unordered List, and it is used to create a list of items marked with bullets (typically round black circles).

`<li><a href="#Home">Home</a></li>`: The `<li>` tag stands for List Item, and is used in conjunction with lists. Inside the list items, `<a>` tags are used for creating hyperlinks. The href attribute specifies the URL of the page the link goes to. In this case, "#" indicates that it's a link to a specific section of the current page.

Note that the `<nav>` tag is not required for all lists of links, but is useful for identifying blocks of major navigation links, and can be particularly helpful in accessibility as it allows screen readers to understand the context of the links.

6. Now you should see this in your browser
  <img width="476" alt="Screenshot 2023-07-14 at 14 27 36" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/69580b80-5c02-417b-9d56-f0c8e4d247f8">
 
### Header
Within the same `<section>` tag as your nag but underneath it place this:
```html
        <div class="main" id="Home">
            <div class="main_content">
                <div class="main_text">
                    <h1>NIKE<br><span>Collection</span></h1>
                    <p>
                        Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has 
                        been the industry's standard dummy text ever since the 1500s, when an unknown printer took 
                        a galley of type and scrambled it to make a type specimen book. It has survived not only 
                        five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.
                    </p>
                </div>
                <div class="main_image">
                    <img src="image/shoes.png">
                </div>
            </div>
            <div class="button">
                <a href="#">SHOP NOW</a>
            </div>
        </div>
```

let's break down each of these tags:

`<div class="main" id="Home">`: This is a div tag, which we've previously discussed. It's being assigned two attributes: a class and an id. The class, "main", can be used to apply styling to this element and any other elements with the same class. The id, "Home", is unique to this element and can be used to target this specific element for CSS or JavaScript. The id also allows this section of the webpage to be directly linked to with a URL that ends in #Home.

`<div class="main_content">`: This div tag is used as a container for grouping together the textual content and the image of the main section. The class "main_content" can be used to style this container.

`<div class="main_text">`: This div tag contains the heading and paragraph for the main section. The class "main_text" can be used to apply styling to this content.

`<h1>NIKE<br><span>Collection</span></h1>`: Here, an h1 tag is used to define the most important heading in the main section. Inside this h1 tag, there is a br tag used to create a line break, and a span tag to distinguish the word "Collection" for unique styling.

`<p>`: The p tag is used to hold the paragraph text for this section.

`<div class="main_image">`: This div tag is used to contain the image for the main section. The class "main_image" can be used to style this container.

`<img src="image/shoes.png">`: The img tag is used to embed an image into the webpage. The src attribute specifies the path to the image file. In this case, the image file is named "shoes.png" and it is located in an "image" folder in the same directory as the HTML file.

`<div class="button">`: This div tag is used as a container for the button and its associated icon. The class "button" can be used to style this element.

`<a href="#">SHOP NOW</a>`: This is an anchor tag (a tag) which is used to create a clickable link. In this case, it's being used to create a "SHOP NOW" button. The href attribute normally specifies the URL that the link leads to. The "#" value is a placeholder and means that this link doesn't actually go anywhere at the moment.

7. Now you should see this in your browser
 <img width="1299" alt="Screenshot 2023-07-14 at 14 41 13" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/6175c8b8-b836-4114-a18d-7b157be1835a">

 ### Styling our Navigation Bar And Header
 So far we have the basic structure of our site thanks to HTML, but you must admit, its very **ugly** lets style our HTML elements using CSS 🔥

 ### What is CSS
CSS is the language we use to style a Web page.

- CSS stands for Cascading Style Sheets
- CSS describes how HTML elements are to be displayed on screen, paper, or in other media
- CSS saves a lot of work. It can control the layout of multiple web pages all at once
- External stylesheets are stored in CSS files

### CSS Solved a Big Problem
HTML was NEVER intended to contain tags for formatting a web page!

HTML was created to describe the content of a web page, like:

`<h1>This is a heading</h1>`

`<p>This is a paragraph.</p>`

When tags like `<font>`, and color attributes were added to the HTML 3.2 specification, it started a nightmare for web developers. Development of large websites, where fonts and color information were added to every single page, became a long and expensive process.

To solve this problem, the World Wide Web Consortium (W3C) created CSS.

CSS removed the style formatting from the HTML page!
  
 ### CSS Syntax
 A CSS rule consists of a selector and a declaration block.
<img width="612" alt="Screenshot 2023-07-14 at 14 47 32" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/27d8bf11-39d5-44f3-9b53-5ba46e8db0de">

The selector points to the HTML element you want to style.

The declaration block contains one or more declarations separated by semicolons.

Each declaration includes a CSS property name and a value, separated by a colon.

Multiple CSS declarations are separated with semicolons, and declaration blocks are surrounded by curly braces.

### CSS Selectors
selectors in CSS are used to target HTML elements and apply styles to them. There are many types of selectors in CSS, each with a specific way of selecting elements. Here are some of the most commonly used ones:

**Type selector**: This is the most basic selector. It matches the name of an HTML element. For example, h1 { color: red; } selects all `<h1>` elements and sets their text color to red.

**Class selector**: This targets elements that have a specific class attribute. It's denoted by a dot (.) followed by the class name. For example, .my-class { color: blue; } selects elements with class="my-class" and sets their text color to blue.

**ID selector**: This targets an element with a specific id attribute. It's denoted by a hash (#) followed by the id name. For example, #my-id { color: green; } selects the element with id="my-id" and sets its text color to green. Remember, IDs should be unique within a page.

**Attribute selector**: This targets elements based on their attributes and attribute values. For example, input[type="text"] { color: purple; } selects `<input>` elements with a type attribute of "text" and sets their text color to purple.

**Pseudo-class selector**: This targets elements in a specific state, like hovered over or focused. For example, a:hover { color: orange; } changes the text color to orange when a link is hovered over with the cursor.

**Pseudo-element selector**: This targets a specific part of an element, like the first letter or line. For example, p::first-letter { font-size: 2em; } makes the first letter of every paragraph twice as big as the rest of the text.

**Descendant combinator**: This targets an element that's a descendant of another element (i.e., nested within it, directly or indirectly). For example, div p { color: yellow; } selects all `<p>` elements that are inside a `<div>`.

**Child combinator**: This targets an element that's a direct child of another element. It's denoted by a > between two selectors. For example, ul > li { color: teal; } selects all `<li>` elements that are direct children of a `<ul>`.

**Adjacent sibling combinator**: This targets an element that's directly after another element at the same level. It's denoted by a + between two selectors. For example, h1 + p { color: brown; } selects the first `<p>` that directly follows an `<h1>`.

**General sibling combinator**: This targets all elements that follow another element at the same level. It's denoted by a ~ between two selectors. For example, h1 ~ p { color: pink; } selects all `<p>` elements that follow an `<h1>` at the same level.

Using these selectors and combinators, you can target pretty much any element on a page in many different ways. Understanding how to use them effectively is a key part of mastering CSS.

### The CSS Box Model
In CSS, the term "box model" is used when talking about design and layout.

The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content. The image below illustrates the box model:
<img width="864" alt="Screenshot 2023-07-14 at 15 26 12" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/42a57db0-f63d-4fbc-9c53-9cfe0ad7307e">

Explanation of the different parts:

**Content** - The content of the box, where text and images appear
**Padding** - Clears an area around the content. The padding is transparent
**Border** - A border that goes around the padding and content
**Margin** - Clears an area outside the border. The margin is transparent

The box model allows us to add a border around elements, and to define space between elements. 

### Positioning in CSS

The position property in CSS determines how an element is positioned in the layout. There are five different position values:

`static`: This is the default value. Elements are positioned according to the normal flow of the document, meaning they are positioned based on where they fall in the HTML.

`relative`: A relative position element is positioned relative to its normal position. Setting the top, right, bottom, and left properties will cause the element to move relative to where it would normally have been.

`absolute`: An absolute position element is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed). If an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.

`fixed`: A fixed position element is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled.

`sticky`: A sticky position element is positioned based on the user's scroll position. It's like relative positioning, but it sticks in place when scrolling hits a specified point (determined by top, right, bottom, or left).

### Display in CSS

The display property in CSS determines how an element is displayed. There are several different display values:

`block`: Block-level elements start on a new line and stretch out to the left and right as far as they can. Examples include `<div>`, `<p>`, and `<h1>`.

`inline`: Inline elements can be placed alongside other elements without breaking the flow of the text. They only take up as much width as their content. Examples include `<span>`, `<a>`, and `<img>`.

`inline-block`: This value is a hybrid of inline and block. It allows the element to sit inline with other elements, but you can still set width and height values like a block element.

`none`: This value makes the element disappear from the page—it's as if it doesn't exist.

`flex`: This value turns the element into a flexible container, making it easier to position and align its children. It's very useful for creating grid-like layouts.

`grid`: This value turns the element into a grid container, making it easier to create complex layouts with rows and columns.
Remember, CSS is all about understanding the relationships between different elements and knowing how to manipulate their display and position to create the desired effect. By mastering the display and position properties, you can take a big step toward creating complex and responsive layouts.

### Sizing in CSS.

CSS has a variety of properties to control the size of elements. You can adjust the width, height, and even max-width, min-width, max-height, and min-height of an element.

`width and height`: These properties are used to set the width and height of an element. By default, these apply to the content box of the element, meaning they don't include padding, borders, or margins. For example, width: 200px; sets the element's width to 200 pixels.

`max-width` and `max-height`: These properties set the maximum width and height an element can expand to. They're very useful for making designs that scale well on different screen sizes. For example, max-width: 100%; ensures that an element won't extend wider than its containing element.

`min-width` and `min-height`: These properties set the minimum width and height an element can shrink to. They're helpful for ensuring that elements don't get too small to be usable or readable.

Apart from these basic properties, there are also some units that you should be aware of:

`Pixels (px)`: A pixel is a dot on the screen, and it's the smallest unit of measurement in screen display. However, on high-resolution devices, a CSS pixel is not always equal to a physical screen pixel.

`Percent (%)`: Percent values are relative to the size of the parent element. For example, width: 50%; makes an element half the width of its parent.

`Viewport units (vw, vh, vmin, vmax)`: These are relative to the viewport size. vw is a percentage of the viewport width, vh is a percentage of the viewport height, vmin is a percentage of the smallest side, and vmax is a percentage of the largest side.

`em` and `rem`: These are relative units based on font sizes. em is relative to the font size of its closest parent, while rem is relative to the root (or html) element's font size. They're very useful for making responsive typography and spacing.

`auto`: This value allows the browser to calculate the size based on other properties and content.

`calc()`: This function allows you to perform calculations to determine CSS property values.

## 3. style.css
Now lets create our first CSS file. Within our editor right click and make a `new file` and name it style.css. In our `index.html` in our `<head>` we are already including our CSS file with this line

`<link rel="stylesheet" href="style.css">`

8. Within `style.css` enter this:
```css
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family:Arial, Helvetica, sans-serif
}

html{
    scroll-behavior: smooth;
}

::-webkit-scrollbar{
    width: 15px;
}

::-webkit-scrollbar-track{
    border-radius: 5px;
    box-shadow: inset 0 0 10px rgba(0,0,0,0.25);
}

::-webkit-scrollbar-thumb{
    border-radius: 5px;
    background: linear-gradient(to top, #c72092 , #6c14d0);
}

section{
    width: 100%;
    height: 100vh;
    background-image: url(image/bg1.png);
    background-size: cover;
    background-position: center;
}

section nav{
    display: flex;
    align-items: center;
    justify-content: space-around;
    box-shadow: 0 0 8px rgba(0,0,0,0.6);
    background: white;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 100;
}

section nav .logo{
    font-size: 35px;
    color: #c72092;
    margin: 5px 0;
    cursor: pointer;
    position: relative;
    left: -4%;
}

section nav .logo span{
    color: #6c14d0;
    text-decoration: underline;
}

section nav ul{
    list-style: none;
}

section nav ul li{
    display: inline-block;
    margin: 5px 15px;
}

section nav ul li a{
    text-decoration: none;
    color: black;
    transition: 0.2s;
}

section nav ul li a:hover{
    color: #c72092;
}

section nav .icons i{
    margin: 0 4px;
    cursor: pointer;
    font-size: 18px;
    transition: 0.3s;
}

section nav .icons i:hover{
    color: #c72092;
}

section .main .main_content{
    display: flex;
    align-items: center;
    justify-content: space-around;
}

section .main .main_content .main_text h1{
    font-size: 90px;
    line-height: 70px;
    font-family: pyxidium quick;
    background: linear-gradient(to right, #c72092,#6c14d0);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    position: relative;
    top: 45px;
    left: 5%;
}

section .main .main_content .main_text h1 span{
    font-size: 70px;
    background: linear-gradient(to right, #c72092,#6c14d0);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

section .main .main_content .main_text p{
    width: 600px;
    text-align: justify;
    line-height: 21px;
    position: relative;
    top: 85px;
    left: 5%;
}

section .main .main_content .main_image img{
    width: 650px;
    position: relative;
    left: 20px;
    top: 75px;
}

section .main .social_icon{
    position: absolute;
    top: 50%;
    left: 98%;
    transform: translate(-50%,-50%);
    font-size: 19px;
}

section .main .social_icon i{
    margin: 8px 0;
    cursor: pointer;
    transition: 0.3s;
}

section .main .social_icon i:hover{
    color: #c72092;
}

section .main .button{
    position: absolute;
    left: 6%;
    padding: 10px 20px;
    border-radius: 30px;
    background: linear-gradient(to right,#c72092 , #6c14d0);
}

section .main .button a{
    color: white;
    text-decoration: none;
}

section .main .button i{
    color: white;
    margin-left: 5px;
    transition: 0.3s;
}

section .main .button:hover i{
    transform: translateX(6px);
}
```

Lets break this down:

`*{...}`: The asterisk is a wildcard selector that matches any element. This rule is applying styles to every element on the page. It's setting margin and padding to 0, which means all elements start with no space around them and no padding inside them. box-sizing: border-box makes the width and height properties include content, padding, and border (but not margin) within the element's total width and height. Lastly, font-family: Arial, Helvetica, sans-serif is setting the default font for the entire webpage to Arial, Helvetica, or the system's default sans-serif font.

`html{...}`: This is applying styles to the root HTML element. scroll-behavior: smooth allows for smooth scrolling when clicking on links that navigate to different parts of the page.

`::-webkit-scrollbar{...}`: This pseudo-element is used to style the scrollbar. In this case, it's setting the scrollbar's width to 15px.

`::-webkit-scrollbar-track{...}` and `::-webkit-scrollbar-thumb{...}`: These are styling the scrollbar's track and thumb (the part you click and drag) respectively. It's giving them rounded corners (border-radius), and the thumb is getting a gradient background color.

`section{...}`: This rule is styling section elements. It's setting the width and height to 100% of the viewport width and height (100vw and 100vh), and it's setting the background image to image/bg1.png, which will cover the entire section and be centered.

`section nav{...}`: This rule is styling nav elements inside section elements. It's making them into a flex container (display: flex), aligning the items along the center of the cross axis (align-items: center), and justifying the content to be evenly distributed in the container (justify-content: space-around). It also adds a shadow (box-shadow), gives it a white background, fixes it to the top of the page (position: fixed) and ensures it always appears on top (z-index: 100).

`section nav .logo{...}`: This rule is styling elements with the class .logo inside nav elements inside section elements. It's setting the font size, color, margin, and so on. Note that cursor: pointer changes the mouse cursor to a pointer when hovering over the logo, indicating it's clickable.

Other rules follow the same pattern, selecting elements based on their tag, class, or hierarchy and applying styles to them. For example, section nav ul li a:hover applies styles to a elements when hovered over, but only if they're inside li elements inside ul elements inside nav elements inside section elements.

The `:hover pseudo-class` is used to apply styles when the mouse hovers over an element. For example, section nav .icons i:hover changes the color of the icons when hovered over.

The transition property adds an animation to an element when its properties change. It can make changes appear more smooth and gradual.
Lastly, the `transform: translateX(6px);` rule moves the element 6px to the right along the X-axis.

9. Lets look in the browser, and BOOM! look at that beauty 🔥 😍
<img width="1446" alt="Screenshot 2023-07-14 at 15 48 56" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/75e11efc-1860-4609-9a55-acefae79dd4e">

### Products Section
This next section contains ALOT of duplication, in upcoming sections we will solve this dont worry! 

10. In your index.html, outside of your closing `</section>` for the nav+header. Enter: 
```html
    <div class="products" id="Products">
        <h1>Products</h1>

        <div class="box">
            <div class="card">
                <div class="image">
                    <img src="image/shoes1.png">
                </div>

                <div class="products_text">
                    <h2>NIKE</h2>
                    <p>
                        Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                    </p>
                    <h3>$100.99</h3>
                    <div class="products_star">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                    </div>
                    <a href="#" class="btn">Add To Cart</a>
                </div>

            </div>

            <div class="card">

                <div class="image">
                    <img src="image/shoes2.png">
                </div>

                <div class="products_text">
                    <h2>NIKE</h2>
                    <p>
                        Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                    </p>
                    <h3>$200.99</h3>
                    <div class="products_star">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star-half-stroke"></i>
                    </div>
                    <a href="#" class="btn">Add To Cart</a>
                </div>

            </div>

            <div class="card">

                <div class="image">
                    <img src="image/shoes3.png">
                </div>

                <div class="products_text">
                    <h2>NIKE</h2>
                    <p>
                        Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                    </p>
                    <h3>$175.99</h3>
                    <div class="products_star">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star-half-stroke"></i>
                        <i class="fa-regular fa-star"></i>
                    </div>
                    <a href="#" class="btn">Add To Cart</a>
                </div>

            </div>

            <div class="card">

                <div class="image">
                    <img src="image/shoes4.png">
                </div>

                <div class="products_text">
                    <h2>NIKE</h2>
                    <p>
                        Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                    </p>
                    <h3>$120.99</h3>
                    <div class="products_star">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-regular fa-star"></i>
                    </div>
                    <a href="#" class="btn">Add To Cart</a>
                </div>

            </div>

            <div class="card">

                <div class="image">
                    <img src="image/shoes5.png">
                </div>

                <div class="products_text">
                    <h2>NIKE</h2>
                    <p>
                        Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                    </p>
                    <h3>$150.99</h3>
                    <div class="products_star">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                    </div>
                    <a href="#" class="btn">Add To Cart</a>
                </div>

            </div>

            <div class="card">

                <div class="image">
                    <img src="image/shoes6.png">
                </div>

                <div class="products_text">
                    <h2>NIKE</h2>
                    <p>
                        Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                    </p>
                    <h3>$220.99</h3>
                    <div class="products_star">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-regular fa-star-half-stroke"></i>
                    </div>
                    <a href="#" class="btn">Add To Cart</a>
                </div>

            </div>

            <div class="card">

                <div class="image">
                    <img src="image/shoes.png">
                </div>

                <div class="products_text">
                    <h2>NIKE</h2>
                    <p>
                        Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                    </p>
                    <h3>$110.99</h3>
                    <div class="products_star">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-regular fa-star"></i>
                        <i class="fa-regular fa-star"></i>
                    </div>
                    <a href="#" class="btn">Add To Cart</a>
                </div>

            </div>

            <div class="card">

                <div class="image">
                    <img src="image/shoes7.png">
                </div>

                <div class="products_text">
                    <h2>NIKE</h2>
                    <p>
                        Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                    </p>
                    <h3>$150.99</h3>
                    <div class="products_star">
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-regular fa-star-half-stroke"></i>
                    </div>
                    <a href="#" class="btn">Add To Cart</a>
                </div>

            </div>

        </div>
    </div>
```

Let's break this down: 

`<div class="products" id="Products">`: This is a div element as we've discussed before, with both class and id attributes. The id attribute is a unique identifier, and it's used here as "Products".

`<h1>Products</h1>`: An h1 element, which we've seen before. It's used here to provide a heading for the page or section.

`<div class="box">`: Another div element with a class attribute. This class of "box" could be styled using CSS to create a container around related content.

`<div class="card">`: This div uses a new class, "card", often used in web design to denote a container for a grouping of related items - in this case, the individual products.

`<div class="image"><img src="image/shoes1.png"></div>`: This is an img tag nested within a div. This structure is commonly used to apply specific styles to the image, such as borders or background colors, that are independent of the image file itself. The img tag's src attribute is set to the path of the image file.

`<div class="products_text">`: This div has a new class, "products_text", which could be used to apply styles to the product's text information.

`<div class="products_star">`: Another new class, "products_star", is applied to this div. This could be used in CSS to style the star rating for each product.

`<a href="#" class="btn">Add To Cart</a>`: This is an a (anchor) element we've seen before. It's used here with a new class, "btn", which could be used in CSS to style the element like a button. When clicked, this button-like link could trigger a JavaScript function to add the product to the cart.

Each div with the class "card" is repeated for each product, with different values for the img source, product name, description, price, and rating. This type of repeated structure is often used in web design for items in a list or grid, like products in an online store.

### Styling The Products Section
11. Now lets style the section, in `style.css` underneath our existing code enter:
```css
.products{
    width: 100%;
    height: 140vh;
    padding: 25px 0;
}

.products h1{
    margin: 35px 0;
    font-size: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    text-transform: uppercase;
    background: linear-gradient(to right, #c72092,#6c14d0);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;    
}

.products .box{
    width: 90%;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-gap: 25px 0;
}

.products .box .card{
    width: 290px;
    height: 440px;
    box-shadow: 0 0 8px #6c14d0;
    border-radius: 5px;
    text-align: center;
    padding: 10px 20px;
    background: #f6f6f6;
}

.products .box .card .small_card{
    display: flex;
    flex-flow: column;
    position: absolute;
    margin: 10px 0;
    transform: translateX(-20px);
    transition: 0.3s;
    opacity: 0;
}

.products .box .card:hover .small_card{
    transform: translateX(2px);
    cursor: pointer;
    opacity: 1;
}

.products .box .card .image{
    display: flex;
    align-items: center;
    justify-content: center;
}

.products .box .card .image img{
    width: 150px;
    margin: 15px 0;
    transition: 0.3s;
}

.products .box .card:hover .image img{
    transform: scale(1.1);
}

.products .box .card .small_card i{
    width: 45px;
    height: 45px;
    border-radius: 5px;
    font-size: 18px;
    margin: 2px 0;
    line-height: 40px;
    border: 2px solid #999999;
    transition: 0.2s;
}

.products .box .card .small_card i:hover{
    color: #c72092;
}

.products .box .card .products_text h2{
    font-size: 30px;
    margin-top: 15px;
}

.products .box .card .products_text p{
    color: #91919191;
    line-height: 21px;
    margin: 8px 0;
}

.products .box .card .products_text h3{
    margin: 7px 0;
}

.products .box .card .products_text .products_star{
    color: orange;
    margin-bottom: 19px;
    cursor: pointer;
}

.products .box .card .products_text .btn{
    text-decoration: none;
    padding: 10px 20px;
    background: linear-gradient(to right, #c72092 , #6c14d0);
    color: white;
}
```

Lets break that down: 

`.products{...}`: Here, all properties have been previously discussed. The CSS is styling the "products" class to occupy the full width of the page and be 140% the height of the viewport. Padding of 25px is applied to the top and bottom.

`.products h1{...}`: The text-transform property changes the text to uppercase. background creates a linear gradient from left to right between two colors. -webkit-background-clip: text; and -webkit-text-fill-color: transparent; are specific to Webkit browsers (like Chrome and Safari) and make the background color show only where there is text, effectively filling the text with the gradient.

`.products .box{...}`: display: grid; establishes a grid container. grid-template-columns: 1fr 1fr 1fr 1fr; creates four equal-width columns. grid-gap: 25px 0; sets the gaps between grid rows and columns. Here, it's creating a 25px gap between rows.

`.products .box .card{...}`: box-shadow: 0 0 8px #6c14d0; adds a shadow to the "card" class. border-radius: 5px; rounds the corners. background: #f6f6f6; changes the background color.

`.products .box .card .small_card{...}`: position: absolute; positions the "small_card" class relative to the nearest positioned ancestor. transform: translateX(-20px); moves the element horizontally. transition: 0.3s; animates changes to CSS properties over time. opacity: 0; makes the element completely transparent.

`.products .box .card:hover .small_card{...}`: This applies styles when the "card" class is hovered over. transform: translateX(2px); moves the "small_card" class 2px to the right. cursor: pointer; changes the cursor to a pointer when hovering. opacity: 1; makes the "small_card" class fully opaque.

`.products .box .card .image img{...}`: transition: 0.3s; adds an animation effect to the "img" class.

`.products .box .card:hover .image img{...}`: This applies styles when the "card" class is hovered over. transform: scale(1.1); enlarges the image to 110% of its original size.

`.products .box .card .small_card i{...}`: border: 2px solid #999999; adds a border to the "i" class elements.

`.products .box .card .small_card i:hover{...}`: This applies styles when "i" class elements within the "small_card" class are hovered over. color: #c72092; changes the color of the text.

`.products .box .card .products_text .btn{...}`: text-decoration: none; removes the underline from links. The padding and background properties have been previously covered. The new background color is a linear gradient, and color: white; changes the color of the text.

12. Looking at this in the browser now should look like:
<img width="1441" alt="Screenshot 2023-07-14 at 16 09 31" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/0b9b0f08-a171-4bd2-a798-4cd6185bc92b">

### About Section
13. In your index.html, outside of your closing products `</div>`. Enter:
```html
<div class="about" id="About">

        <h1>Web<span>About</span></h1>

        <div class="about_main">
            <div class="about_image">
                <div class="about_small_image">
                    <img src="image/red_shoes1.png" onclick="updateMainImage(this)">
                    <img src="image/red_shoes2.png" onclick="updateMainImage(this)">
                    <img src="image/red_shoes3.png" onclick="updateMainImage(this)">
                    <img src="image/red_shoes4.png" onclick="updateMainImage(this)">
                </div>

                <div class="image_contaner">
                    <img src="image/red_shoes1.png" id="imagebox">
                </div>

            </div>

            <div class="about_text">
                <p>
                    Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of
                    classical
                    Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at
                    Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from
                    a
                    Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the
                    undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of "de Finibus Bonorum et
                    Malorum"
                    (The Extremes of Good and Evil) by Cicero, written in 45 BC. This book is a treatise on the theory
                    of ethics,
                    very popular during the Renaissance. The first line of Lorem Ipsum, "Lorem ipsum dolor sit amet..",
                    comes
                    from a line in section 1.10.32. The standard chunk of Lorem Ipsum used since the 1500s is reproduced
                    below
                    for those interested. Sections 1.10.32 and 1.10.33 from "de Finibus Bonorum et Malorum" by Cicero
                    are also
                    reproduced in their exact original form, accompanied by English versions from the 1914 translation
                    by H. Rackham.
                </p>
            </div>

        </div>

        <a href="#" class="about_btn">Shop Now</a>

        <script>
            function updateMainImage(small) {
                var full = document.getElementById("imagebox")
                full.src = small.src
            }
        </script>

    </div>
```

Let's break this down: 


`<h1>Web<span>About</span></h1>`: This line uses a `<span>` element within the `<h1>` element. The `<span>` tag is used for grouping inline-elements in a document and can be used to apply styles to the contained text or to perform certain tasks with JavaScript.
    
`<div class="about_image"> and <div class="image_contaner">`: These are new divisions used to organize images.
    
`<img src="image/red_shoes1.png" onclick="updateMainImage(this)">`: This is an img element similar to ones seen before, but it now has an onclick attribute. This attribute specifies a JavaScript function (updateMainImage(this)) to be executed when the element is clicked.
    
`function updateMainImage(small) { var full = document.getElementById("imagebox") full.src = small.src }`: This is an inline JavaScript function. When a smaller image is clicked, this function changes the source of the main image to match that of the clicked image.

`<div class="about_text">`: This division contains text about the product. Inside it, the <p> element encloses a block of text.

`<a href="#" class="about_btn">Shop Now</a>`: This is a link element with the class "about_btn". When clicked, it might lead the user to a shopping page. The actual link is not specified here (denoted by the "#").

### Styling The About Section
14. Now lets style the section, in `style.css` underneath our existing code enter:
```css
.about{
    width: 100%;
    height: 100vh;
    padding: 35px 0;
}

.about h1{
    font-size: 60px;
    margin-top: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
    background: black;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    text-transform: uppercase;
}

.about h1 span{
    background: linear-gradient(to right, #c72092 , #6c14d0);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-left: 15px;
}

.about .about_main{
    position: relative;
    top: 40%;
    left: 50%;
    transform: translate(-50%,-50%);
    display: flex;
    justify-content: space-around;
    align-items: center;
}

.about .about_main .about_image{
    display: flex;
    margin-top: 50px;
}

.about .about_main .about_image .about_small_image{
    display: flex;
    flex-direction: column;
    position: relative;
    top: 15px;
}

.about .about_main .about_image .about_small_image img{
    height: 92px;
    margin: 5px 0;
    cursor: pointer;
    background: linear-gradient(to right, #6c14d0 , #c72092);
    display: block;
    border-radius: 6px;
    padding: 5px 5px;
    box-shadow: 0 0 6px rgba(0,0,0,0.6);
    opacity: 0.8;
    transition: 0.3s;
}

.about .about_main .about_image .about_small_image img:hover{
    opacity: 1;
}

.about .about_main .image_contaner{
    padding: 10px;
    display: flex;
}

.about .about_main .image_contaner img{
    border: 3px solid #6c14d0;
    border-radius: 20px;
    height: 430px;
    padding: 30px;
    box-shadow: 0 0 8px #6c14d0;
}

.about .about_main .about_text{
    margin-top: 45px;
}

.about .about_main .about_text p{
    background: linear-gradient(to left, #c72092 , #6c14d0);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    line-height: 22px;
    width: 600px;
    text-align: justify;
    padding: 25px 30px;
    border: 2px solid #c72092;
    border-radius: 20px;
    box-shadow: 0 0 8px #c72092;
}

.about .about_btn{
    color: black;
    background: none;
    position: relative;
    top: 10%;
    left: 50%;
    transform: translate(-50% , -50%);
    padding: 10px 25px;
    border: 2px solid #c72092;
    text-decoration: none;
    box-shadow: 0 0 8px #c72092;
    transition: 0.5s;
}

.about .about_btn:hover{
    border: 2px solid transparent;
    background: #c72092;
    color: white;
}
```

Let's break that down:

`position: relative;`: This property positions an element relative to its normal position. Other elements will not adjust to fit into space when it is moved. When combined with top, left, right, bottom, it allows the element to be moved in the respective direction.

`transform: translate(-50%,-50%);`: The transform property modifies the coordinate space of an element using the translate function. In this case, the element is moved left by 50% of its width and up by 50% of its height. This is often used to center an element.

`justify-content: space-around;`: This is a flexible box layout specific property (works when display is set to flex). It defines how space is distributed between and around items along the main axis (in this case, horizontally). space-around means items have a half-size space on both ends, and a full-size space between them.

`background: linear-gradient(to left, #c72092 , #6c14d0);`: This sets a linear gradient background image. The direction of the gradient is to left, which means the gradient starts from the right.

`text-align: justify;`: This property sets the text alignment to justify. The text is spread to align with both the left and right margins.

`box-shadow: 0 0 8px #c72092;`: The box-shadow property applies a shadow to an element. The first and second values specify the horizontal and vertical offsets, the third is the blur radius, and the last value specifies the color of the shadow.

`transition: 0.5s;`: The transition property is a shorthand property for transition-property, transition-duration, transition-timing-function, and transition-delay. Here, it's set to last 0.5 seconds, and it applies to all changeable properties.

`The :hover pseudo-class`: This is a CSS pseudo-class that matches when the user interacts with an element with a pointing device, but does not necessarily activate it. It is generally used to control color changes, underlines, backgrounds, and cursors, in response to the user hovering over an element.

15. Looking at the result in the browser, it should look like:
<img width="1666" alt="Screenshot 2023-07-14 at 16 24 57" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/47462488-d6f7-461c-9a51-93b0065de8fd">


### Review Section
This section also involes some duplication, but dont worry! 

16. In your index.html, outside of your closing about </div>. Enter:
```html
    <div class="review" id="Review">
        <h1>Customer's<span>review</span></h1>
        
        <div class="review_box">
            <div class="review_card">
                <div class="card_top">
                    <div class="profile">

                        <div class="profile_image">
                            <img src="image/girl_dp1.jpg">
                        </div>

                        <div class="name">
                            <strong>Ranidi Lochana</strong>

                            <div class="like">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                            </div>
                        </div>

                    </div>
                </div>
                <div class="comment">
                    <p>
                        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Debitis, amet nesciunt voluptatem cum 
                        architecto ipsum vero nulla voluptatibus dolorum modi assumenda eum? Aliquid inventore velit ipsa 
                        repellat numquam atque dolores!
                    </p>
                </div>
            </div>   

            <div class="review_card">
                <div class="card_top">
                    <div class="profile">

                        <div class="profile_image">
                            <img src="image/man_dp1.jpg">
                        </div>

                        <div class="name">
                            <strong>Sayuru Tharanga</strong>

                            <div class="like">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                                <i class="fa-regular fa-star"></i>
                            </div>
                        </div>

                    </div>
                </div>
                <div class="comment">
                    <p>
                        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Debitis, amet nesciunt voluptatem cum 
                        architecto ipsum vero nulla voluptatibus dolorum modi assumenda eum? Aliquid inventore velit ipsa 
                        repellat numquam atque dolores!
                    </p>
                </div>
            </div>   

            <div class="review_card">
                <div class="card_top">
                    <div class="profile">

                        <div class="profile_image">
                            <img src="image/man_dp2.jpg">
                        </div>

                        <div class="name">
                            <strong>Senuda Dilwan</strong>

                            <div class="like">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                                <i class="fa-regular fa-star"></i>
                                <i class="fa-regular fa-star"></i>
                            </div>
                        </div>

                    </div>
                </div>
                <div class="comment">
                    <p>
                        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Debitis, amet nesciunt voluptatem cum 
                        architecto ipsum vero nulla voluptatibus dolorum modi assumenda eum? Aliquid inventore velit ipsa 
                        repellat numquam atque dolores!
                    </p>
                </div>
            </div>   

        </div>

        <div class="review_box">
            <div class="review_card">
                <div class="card_top">
                    <div class="profile">

                        <div class="profile_image">
                            <img src="image/gir_dp3.jpg">
                        </div>

                        <div class="name">
                            <strong>Kaveesha Vidurangi</strong>

                            <div class="like">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                                <i class="fa-regular fa-star"></i>
                            </div>
                        </div>

                    </div>
                </div>
                <div class="comment">
                    <p>
                        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Debitis, amet nesciunt voluptatem cum 
                        architecto ipsum vero nulla voluptatibus dolorum modi assumenda eum? Aliquid inventore velit ipsa 
                        repellat numquam atque dolores!
                    </p>
                </div>
            </div>   

            <div class="review_card">
                <div class="card_top">
                    <div class="profile">

                        <div class="profile_image">
                            <img src="image/gir_dp2.jpg">
                        </div>

                        <div class="name">
                            <strong>John Deo</strong>

                            <div class="like">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                            </div>
                        </div>

                    </div>
                </div>
                <div class="comment">
                    <p>
                        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Debitis, amet nesciunt voluptatem cum 
                        architecto ipsum vero nulla voluptatibus dolorum modi assumenda eum? Aliquid inventore velit ipsa 
                        repellat numquam atque dolores!
                    </p>
                </div>
            </div>   

            <div class="review_card">
                <div class="card_top">
                    <div class="profile">

                        <div class="profile_image">
                            <img src="image/man_dp3.jpg">
                        </div>

                        <div class="name">
                            <strong>Charith Aruna</strong>

                            <div class="like">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                            </div>
                        </div>

                    </div>
                </div>
                <div class="comment">
                    <p>
                        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Debitis, amet nesciunt voluptatem cum 
                        architecto ipsum vero nulla voluptatibus dolorum modi assumenda eum? Aliquid inventore velit ipsa 
                        repellat numquam atque dolores!
                    </p>
                </div>
            </div>   

        </div>

    </div>
```

Let's break this down: 

`<strong>Ranidi Lochana</strong>`: The `<strong>` HTML element indicates that its contents have strong importance, seriousness, or urgency. Browsers typically render the contents in bold type.

### Styling the Reviews Section
17. Now lets style the section, in `style.css` underneath our existing code enter:
```css
.review{
    width: 100%;
    height: 100vh;
    padding-top: 80px;
}

.review h1{
    font-size: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 30px;
    text-transform: uppercase;
}

.review h1 span{
    background: linear-gradient(to left, #c72092 , #6c14d0);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-left: 15px;    
}

.review .review_box{
    width: 95%;
    position: relative;
    top: 7%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
}

.review .profile .profile_image{
    width: 60px;
    height: 60px;
    border-radius: 50%;
    overflow: hidden;
    margin: 5px 0;
    box-shadow: 0 0 10px rgba(0,0,0,0.5);
    cursor: pointer;
    transition: 0.3s;
}

.review .profile .profile_image:hover{
    transform: scale(1.2);
}

.review .profile_image img{
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
}

.review .profile{
    display: flex;
    align-items: center;
}

.review .review_box .review_card{
    width: 500px;
    background: #f3f1f1;
    padding: 20px 25px;
    border-radius: 5px;
    margin: 15px;
    box-shadow: 0 0 10px rgba(0,0,0,0.3);
}

.review .review_box .review_card .card_top{
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.review .review_box .review_card .card_top .profile .name{
    margin-left: 20px;
    line-height: 22px;
}

.review .review_box .review_card .card_top .profile .name strong{
    font-size: 20px;
}

.review .review_box .review_card .card_top .profile .name .like i{
    color: orange;
    display: inline-block;
    font-size: 12px;
}

.review .review_box .review_card .comment p{
    text-align: justify;
    line-height: 22px;
    margin-top: 15px;
}
```

Let's break this down: 

`height: 100vh;`: Here, vh stands for viewport height. It's a relative unit that means "1% of the height of the viewport". So height: 100vh; will make the element take up the entire height of the viewport.

`linear-gradient(to left, #c72092 , #6c14d0);`: The linear-gradient() function creates an image consisting of a progressive transition between two or more colors along a straight line. Its result is an object of the `<image>` data type, which can be used as a value of the background-image property. In this case, the gradient is going from right to left (specified by to left) starting from color #c72092 and ending with color #6c14d0.

`-webkit-background-clip: text;`: The -webkit-background-clip CSS property determines whether an element's background, either the color or image, extends underneath its border. Here, it's being used with the value text, which will cause the background to clip to the foreground text. Note that this is a non-standard feature and it's not fully supported in all browsers.

`-webkit-text-fill-color: transparent;`: The -webkit-text-fill-color CSS property specifies the fill color of characters of text. In this case, it's used to make the text transparent, which lets the background-clip effect show through.

`object-fit: cover;`: The object-fit CSS property sets how the content of a replaced element, such as an <img> or <video>, should be resized to fit its container. cover scales the image to fill the element's content box, while preserving its aspect ratio.

`object-position: center;`: The object-position property determines the position of the replaced content within the content box, when the content does not completely fill the content box.

`transform: scale(1.2);`: The transform CSS property lets you rotate, scale, skew, or translate an element. Here, it's used with scale(1.2), which means the image will grow to 120% of its original size when hovered over.

`transition: 0.3s;`: The transition property is a shorthand property for transition-property, transition-duration, transition-timing-function, and transition-delay. It allows elements to change values over a specified duration. Here it's set to 0.3s, meaning that any change will transition smoothly over a 300 millisecond period.

18. Looking in the browser, it should now look like:
<img width="1664" alt="Screenshot 2023-07-14 at 16 40 58" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/0b810c5d-eb0b-4693-9f4e-893e086f4a53">

### Services Section
19. In your index.html, outside of your closing review </div>. Enter:
```html
    <div class="services" id="Servises">
        <h1>our<span>services</span></h1>

        <div class="services_cards">
            <div class="services_box">
                <i class="fa-solid fa-truck-fast"></i>
                <h3>Fast Delivery</h3>
                <p>
                    Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                </p>
            </div>

            <div class="services_box">
                <i class="fa-solid fa-rotate-left"></i>
                <h3>10 Days Replacement</h3>
                <p>
                    Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                </p>
            </div>

            <div class="services_box">
                <i class="fa-solid fa-headset"></i>
                <h3>24 x 7 Support</h3>
                <p>
                    Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                </p>
            </div>
        </div>

    </div>
```

No new topics have been introduced here!

### Styling The Services Section
20. Now lets style the section, in `style.css` underneath our existing code enter:
```css
.services{
    width: 70%;
    margin: 0 auto;
    text-align: center;
    padding: 80px 0 10px 0;
}

.services h1{
    font-size: 60px;
    text-transform: uppercase;
}

.services h1 span{
    margin-left: 15px;
    background: linear-gradient(to left, #c72092 , #6c14d0);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;    
}

.services .services_cards{
    width: 80%;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: relative;
    top: 50px;
}

.services .services_box i{
    font-size: 60px;
    color: orange;
    margin: 20px 0;
    cursor: pointer;
}

.services .services_box h3{
    margin-bottom: 12px;
    font-size: 19px;
}

.services .services_box p{
    text-align: center;
    color: #919191;
    margin-bottom: 60px;
}
```

No new topics have been introduced here!

21. Looking in the browser, it should now look like:
<img width="1764" alt="Screenshot 2023-07-14 at 16 46 22" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/1035073b-48af-40d6-bd6f-b3c5c702b4c6">

### Login From Section
22. In your index.html, outside of your closing services </div>. Enter:

```html
    <div class="login_form">
        <div class="left">
            <img src="image/logshoes.png">
        </div>

        <div class="right">
            <h1>Welcome Back!</h1>

            <form action="#" method="post">
                <p>User Name</p>
                <div class="user">
                    <i class="fa-solid fa-user"></i>
                    <input type="text" name="user" placeholder="User Name" class="username">
                </div>

                <p class="passworg_tag">Password</p>
                <div class="password">
                    <i class="fa-solid fa-lock"></i>
                    <input type="text" name="password" placeholder="Password">
                </div>

                <p class="forget">Forget Password ?</p>

                <button type="submit">Login</button>
                <div class="loging_icon">
                    <a href="#"><img src="image/google.png"></a>
                    <a href="#"><img src="image/facebook.png"></a>
                    <a href="#"><img src="image/twitter.png"></a>
                </div>

            </form>

        </div>

    </div>
```

Let's break down the new concepts:

`<form action="#" method="post">`: The action attribute specifies where to send the form data when the form is submitted. In this case, action="#" is a placeholder and would typically be replaced with the URL of a server-side script (such as a PHP page) to process the form data. The method attribute specifies the HTTP method (get or post) to use when sending the form data. post is used when the form data should be sent within the body of the HTTP request, which is more secure as the data does not show up in the URL.
    
`<button>`: The HTML `<button>` element represents a clickable button.

### Styling The Login Form Section
23. Now lets style the section, in `style.css` underneath our existing code enter:
```css
.login_form{
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-image: url(image/loging_bg.png);
    background-size: cover;
    background-position: center;
}

.login_form .left img{
    width: 650px;
}

.login_form .right{
    position: relative;
    top: -50px;
    left: -60px;
    padding: 50px 80px;
}

.login_form .right h1{
    font-family: prevattscriptssk;
    font-size: 45px;
    margin-bottom: 40px;
}

.login_form .right p{
    margin-bottom: 5px;
}

.login_form .right .user{
    border: 2px solid #6c14d0;
    border-radius: 5px;
    width: 350px;
    height: 40px;
    display: flex;
}

.login_form .right .user i{
    position: relative;
    top: 9px;
    left: 15px;
    color: #c72092;
}

.login_form .right .user .username{
    position: relative;
    left: 9%;
    width: 295px;
    background: none;
    outline: none;
    border: none;
    display: flex;
    font-size: 15px;
}

.login_form .right .passworg_tag{
    margin: 15px 0 5px 0;
}

.login_form .right .password{
    border: 2px solid #6c14d0;
    border-radius: 5px;
    width: 350px;
    height: 40px;
    display: flex;
}

.login_form .right .password i{
    position: relative;
    top: 9px;
    left: 15px;
    color: #c72092;
}

.login_form .right .password input{
    position: relative;
    left: 9%;
    width: 295px;
    background: none;
    border: none;
    outline: none;
    display: flex;
    font-size: 15px;
}

::-webkit-input-placeholder{
    color: black;
    opacity: 0.7;
}

.login_form .right .forget{
    position: relative;
    left: 60%;
    margin: 6px 0 10px 0;
    cursor: pointer;
}

.login_form .right button{
    width: 350px;
    color: white;
    padding: 7px 20px;
    border: none;
    border-radius: 5px;
    font-size: 20px;
    cursor: pointer;
    background: linear-gradient(to right, #c72092 , #6c14d0);
}

.login_form .right .loging_icon{
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 25px;
}

.login_form .right .loging_icon a{
    width: 30px;
    height: 30px;
    margin: 0 2px;
    border-radius: 50%;
    background: #f3f3f3;
    box-shadow: 0 0 5px rgba(0,0,0,0.6);
}

.login_form .right .loging_icon img{
    width: 20px;
    margin: 5px 5px;
}
```

Lets breakdown the new concepts introduced: 

`background-image`: url(image/loging_bg.png);: This property sets an image as the background of an element. The image file path is placed within the URL() function.

`background-size: cover;`: This property specifies the size of the background images. The cover value scales the background image to be as large as possible so that the area of the element is completely covered by the background image. This may mean the image is cropped to preserve its aspect ratio.

`background-position: center;`: This property sets the initial position of a background image. The center value means the image is positioned at the center of the element.

`position: relative;`: This property sets the type of positioning method used for an element. relative means the position is set relative to its normal position. This doesn't itself move the element, but it affects the positions of other properties like top, right, bottom, left.

`top: -50px;`: This property affects the vertical position of a positioned element. This property has no effect on non-positioned elements. Here it's shifting the element 50 pixels upwards from its normal position because of the negative value.

`left: -60px;`: This property affects the horizontal position of a positioned element. Here it's shifting the element 60 pixels to the left of its normal position because of the negative value.

`border: 2px solid #6c14d0;`: This is a shorthand property for setting the border-width, border-style, and border-color of an element in a single declaration. Here it's creating a 2 pixel wide, solid border with the color #6c14d0.

`border-radius: 5px;`: This property allows you to add rounded borders to an element. Here, it's setting a 5 pixel radius to round the corners of the border.

`outline: none;`: This property sets the outline of an element. none means the element will have no outline.

`::webkit-input-placeholder { color: black; opacity: 0.7; }`: This is a pseudo-element that allows you to style the placeholder text in input fields. The -webkit- prefix is used for Chrome, Safari, and newer versions of Opera. Here it's setting the color of the placeholder text to black with 70% opacity.

`box-shadow: 0 0 5px rgba(0,0,0,0.6);`: This property adds shadow effects around an element's frame. The values correspond to horizontal offset, vertical offset, blur radius, and color of the shadow respectively. Here, it's creating a shadow with 5px blur radius, and a semi-transparent black color (60% opacity).


24. Looking in the browser, it should now look like:
<img width="1658" alt="Screenshot 2023-07-14 at 16 59 31" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/ed579f14-9ba6-4d7d-bcd4-ba06044cf519">


### Footer Section
25. In your index.html, outside of your closing login_form </div>. Enter:
```html
    <footer>
        <div class="footer_main">
            <div class="tag">
                <h1>Contact</h1>
                <a href="#"><i class="fa-solid fa-house"></i>123/Middlesbrough/United Kingdom</a>
                <a href="#"><i class="fa-solid fa-phone"></i>+94 12 345 6789</a>
                <a href="#"><i class="fa-solid fa-envelope"></i>contact@gmail.com</a>
            </div>

            <div class="tag">
                <h1>Get Help</h1>
                <a href="#" class="center">FAQ</a>
                <a href="#" class="center">Shipping</a>
                <a href="#" class="center">Returns</a>
                <a href="#" class="center">Payment Options</a>
            </div>

            <div class="tag">
                <h1>Our Stores</h1>
                <a href="#" class="center">UK</a>
                <a href="#" class="center">Japan</a>
            </div>

            <div class="tag">
                <h1>Newsletter</h1>
                <div class="search_bar">
                    <input type="text" placeholder="You email here">
                    <button type="submit">Subscribe</button>
                </div>
            </div>

        </div>
    </footer>
```

Let's break the new concepts down: 

The `<footer>` tag is used to define a footer for a document or a section. A footer typically contains information about the author of the section, copyright information, links to terms of use, contact information, etc.

### Styling The Footer Section
26. Now lets style the section, in `style.css` underneath our existing code enter:
```css
footer{
    width: 100%;
}

footer .footer_main{
    width: 100%;
    background: #f3f1f1;
    display: flex;
    justify-content: space-around;
}

footer .footer_main .tag{
    margin: 10px 0;
}

footer .footer_main .tag .center{
    text-align: center;
}

footer .footer_main .tag h1{
    font-size: 25px;
    margin: 25px 0;
    color: #1c0080;
}

footer .footer_main .tag a{
    display: block;
    color: black;
    text-decoration: none;
    margin: 9px 0;
}

footer .footer_main .tag a i{
    padding: 0 10px;
    transition: 0.3;
}

footer .footer_main .tag a i:hover{
    color: #c72092;
}

footer .footer_main .tag .social_link{
    display: flex;
}

footer .footer_main .tag .social_link a{
    width: 30px;
    height: 30px;
    border-radius: 50%;
    text-align: center;
    text-decoration: none;
    color: black;
    box-shadow: 0 0 20px 10px rgba(0,0,0,0.05);
    position: relative;
    margin: 0 5px;
    z-index: 10;
    overflow: hidden;
}

footer .footer_main .tag .social_link a .fa-brands{
    font-size: 15px;
    line-height: 30px;
    z-index: 10;
    position: relative;
    transition: 0.5s;
}

footer .footer_main .tag .social_link a:hover i{
    color: white;
}

footer .footer_main .tag .social_link a::after{
    content: '';
    width: 100%;
    height: 100%;
    top: 0;
    left: -90px;
    background: linear-gradient(-45deg, #c72092 , #6c14d0);
    position: absolute;
    z-index: -10;
    transition: 0.5s;
}

footer .footer_main .tag .social_link a:hover::after{
    left: 0;
}

footer .footer_main .tag .search_bar{
    width: 230px;
    height: 30px;
    background: rgb(202, 202, 202);
    border-radius: 25px;
}

footer .footer_main .tag .search_bar input{
    width: 200px;
    padding: 2px 0;
    position: relative;
    top: 17%;
    left: 6%;
    border: none;
    background: none;
    outline: none;
    font-size: 13px;
}

footer .footer_main .tag .search_bar button{
    padding: 7px 15px;
    background: linear-gradient(to right, #c72092 , #6c14d0);
    border: none;
    margin-top: 15px;
    border-radius: 25px;
    color: white;
    cursor: pointer;
}
```

This introcues no new concepts 🙌🏻

27. Looking in the browser, it should now look like:
<img width="1631" alt="Screenshot 2023-07-14 at 17 09 45" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/3a751749-ab38-4d1a-88f1-fc992f76ec8e">

# Congratulations 🎉🎉🎉🎉🎉
Congratulations! Your hard work, dedication, and determination have truly paid off. Building a website from scratch is no easy feat, especially when diving deep into the intricacies of HTML and CSS. However, you've not only built a beautifully designed store landing page, but also acquired a deep understanding of each and every concept used to bring this project to life. This accomplishment is a testament to your passion for web development and your commitment to learning. Remember, each line of code you wrote is a step forward on your journey. May this success lead to a greater achievement in the years to come. Keep coding, keep learning, and keep pushing the boundaries of what's possible. Well done!
![image](https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/b4b45ae0-2251-485e-b173-59fa912023ef)

