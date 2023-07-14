# 👋🏻 Hi, hello and welcome to the team!
![image](https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/d2b1d5d4-cbc1-4d8b-8671-4abe42e71f30)

## Introduction
Becoming a software engineer can be overwhelming! You will hear so many different languages and frameworks being mentioned that you may think, what on earth have I signed myself up for. 

But dont worry, We have **all** been there 🙋🏼‍♂️. 

I have purposely designed this demo project to take you through the **basics** and slowly move onto more advanced concepts as we progress our skills and when it feels right, instead of throwing everything at you all at once.  

## Course Structure 
A break down of the course is: 
- **Project Breif**  - Here we will describe what we are going to be building together, I will show you the completed project Blue Peter style.

- **Static HTML/CSS site** - We will cover the badics of HTML and CSS, we will understand how they work together
  
- **Vue.js refactor** - We will convert our static site into a Vue.js app. We will discuss the advantages to this as well as cover the basics of Vue.js
  
- **Laravel API** - We wil create a seperate project which our Vue.js app can communicate with
  
- **Further Advancements** - We will discuss how we can build upon the skills we have learnt in the previous chapters can be utlised to add brand new features/functionality to our app.

# Project Breif
<img width="1762" alt="Screenshot 2023-07-14 at 11 30 41" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/16c6c946-0018-4282-820c-51a1458a893c">

[Video link](https://www.youtube.com/watch?v=bubzArfuxVo)

**Title**: E-commerce Store Landing Page Development for Nike Trainers

**Objective**: The aim of this project is to create a user-friendly, engaging, and visually appealing landing page for an e-commerce store that primarily sells Nike trainers.

**Description**: The landing page will be simple but detailed, comprising several sections. Each section will serve a specific purpose and contribute to the overall user experience:

- **Hero Section**: The introductory section will captivate visitors with an attractive headline, sub-heading, and a compelling call-to-action (CTA) button.
  
- **Product Display Section**: There will be dedicated areas to showcase a variety of Nike trainers, both popular and new arrivals, to cater to different customer preferences.

- **About Section**: A section that provides information about the e-commerce store and its mission. This will help to build a stronger connection with customers and foster trust in the brand.

- **Review Section**: This section will exhibit customer testimonials and ratings, helping to build trust among potential buyers.
Services Section: This area will highlight the e-commerce store's unique selling propositions such as fast delivery, a 10-day replacement policy, and round-the-clock customer support.

- **Login Form**: A simple and secure login form for users to access their accounts.
  
- **Footer Section**: The footer will contain important links and information including contact details, FAQ, shipping and return policies, and payment options. Additionally, a newsletter subscription form will be provided to engage users in a long-term relationship.

## Work Items
Work-items are essentially the smaller tasks that make up a larger project or goal. The concept of work-items comes from agile development methodologies, which focus on iterative and incremental delivery of software. Breaking down a project into smaller, manageable tasks, or "work-items," is a key aspect of this approach.

Here's why we break tasks down into work-items:

**Manageability**: Large projects can be overwhelming. By breaking the project down into smaller work-items, the tasks become more manageable. Each work-item can be tackled independently, making the work more approachable and less daunting.

**Organization**: Work-items help to keep the project organized. They can be tracked, prioritized, and managed individually, which makes the project as a whole easier to oversee.

**Estimation**: By breaking down the project into work-items, it's easier to estimate how long each part of the project will take. This can help with scheduling and resource allocation.

**Progress Tracking**: Work-items allow for easy progress tracking. When a work-item is completed, it's a clear indication of progress being made on the project. This not only keeps the team aware of where they are but also provides a motivational boost.

**Flexibility**: If the project needs to change direction or scope, having individual work-items makes it easier to adjust. Tasks can be added, removed, or re-prioritized without affecting the entire project.

**Collaboration**: Work-items can be assigned to different team members based on their skills and capabilities, promoting collaboration and efficient utilization of resources.

In essence, work-items make large projects more manageable, organized, and adaptable. They support efficient tracking of progress and resource allocation, and foster a collaborative work environment.

## Work Items For This Project

**HTML Structure Work-item**:
WHEN I am structuring the HTML, I WANT to create clear and organized markup, SO THAT the webpage is easy to understand and modify in the future.

**About Section Work-item**:
WHEN I am creating the "About" section, I WANT to provide engaging and concise information about the store, SO THAT users can understand more about us and our values.

**Product Display Section Work-item**:
WHEN I am creating the product display section, I WANT to highlight popular and new arrival Nike trainers, SO THAT users can easily browse and select products.

**Review Section Work-item**:
WHEN I am coding the review section, I WANT to create a simple list structure, SO THAT reviews and ratings are displayed in a user-friendly manner.

**Services Section Work-item**:
WHEN I am creating the "Services" section, I WANT to use relevant icons and descriptions, SO THAT users can understand the services we offer quickly.

**Login Form Work-item**:
WHEN I am building the login form, I WANT to ensure it collects username and password correctly, SO THAT it can be used for user authentication.

**Footer Section Work-item**:
WHEN I am creating the footer, I WANT to include all necessary information like contact details, help links and newsletter subscription form, SO THAT users can find additional information and contact us if needed.

**Styling Work-item**:
WHEN I am styling the webpage, I WANT to use CSS effectively, SO THAT the webpage looks appealing and matches the design mockups.

**Testing Work-item**:
WHEN I am testing the webpage, I WANT to ensure it displays correctly in different browsers, SO THAT all users have a consistent viewing experience.

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
The `<!DOCTYPE html>` declaration defines that this document is an HTML5 document
The `<html>` element is the root element of an HTML page
The `<head>` element contains meta information about the HTML page
The `<title>` element specifies a title for the HTML page (which is shown in the browser's title bar or in the page's tab)
The `<body>` element defines the document's body, and is a container for all the visible contents, such as headings, paragraphs, images, hyperlinks, tables, lists, etc.
The `<h1>` element defines a large heading
The `<p>` element defines a paragraph

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

**<meta charset="UTF-8">**: The <meta> tag provides metadata about the HTML document. Metadata isn't displayed on the page but is machine parsable. In this case, the charset attribute specifies the character encoding for the HTML document. UTF-8 is a universal character set that includes all characters from all writing systems, so it's good practice to use this to support international characters and symbols.

**<meta http-equiv="X-UA-Compatible" content="IE=edge">**: This <meta> tag is used for compatibility with Internet Explorer. It tells IE to display the webpage in the highest mode available, thus ensuring the webpage uses the latest rendering engine. edge means the very latest version that IE has to offer.

**<meta name="viewport" content="width=device-width, initial-scale=1.0">**: This <meta> tag is used for responsive web design. It sets the width of the page to follow the screen-width of the device (which will vary depending on the device). The initial-scale=1.0 part sets the initial zoom level when the page is first loaded by the browser.

**<link rel="stylesheet" href="style.css">**: The <link> tag defines the relationship between the current document and an external resource. In this case, it's linking to an external CSS file (style.css) which provides the styles for the HTML document. The rel attribute specifies the relationship as a "stylesheet".

**<link rel="shortcut icon" href="image/logo.png">**: This <link> tag is used to specify a shortcut icon or favicon for the HTML document. The favicon is a small icon that appears in the browser tab next to the webpage's title. The href attribute specifies the path to the image file.