# Vue.js_refactor

By the end of this section you will have converted our static website into a Vue.js application 🚀

## Why Add JavaScript to Our Site?

JavaScript is a programming language that can add dynamic and interactive elements to your website. This means your website will be able to do more than just display static information; it can respond to user inputs, update in real-time, and create a more engaging user experience.

Here are some key reasons why we add JavaScript to a website:

**Interactivity**: JavaScript enables a site to respond immediately to user actions, creating an interactive experience. For example, a user could click a button to show or hide more information without the page needing to reload.

**Dynamism**: JavaScript makes it possible to create content that updates dynamically. A countdown timer, for instance, updates every second without requiring a page refresh.

**Front-End Control**: JavaScript can be used to change the way your website looks and behaves in response to user input or other factors. You can use it to validate form inputs, manipulate elements on the webpage, create animations, and much more.

**API Interaction**: JavaScript can also interact with web APIs (Application Programming Interfaces), which are sets of rules that allow different software applications to communicate with each other. This can enable features like fetching updated data from a server or storing data on a user's browser for later use.

## What is a Framework and Why Use One?

A software framework is like a blueprint: it provides a basic structure where you can fill in the specifics. It helps you to build your software by providing a structure and reusable code to perform common tasks.

**Think of it like building a model car**: you could craft every piece by hand, but it's much easier if you start with a kit that provides pre-formed parts. You just need to put them together.

**Efficiency**: A framework like Vue.js provides many built-in functions and tools that developers commonly need, so you don't have to build everything from scratch.

**Structure**: A framework gives your code a specific structure, making it easier for you and others to read and maintain. It's like following a set of best practices.

**Security**: Frameworks often have built-in protections against common web security risks, such as Cross-Site Scripting (XSS) and SQL injection attacks.
Community Support: A popular framework has a community of thousands or even millions of developers who can offer help, create plugins to extend the functionality, and continually improve the framework.

**Focus on Business Logic**: By handling many routine tasks, a framework lets you concentrate on the unique features of your application, which is often referred to as the "business logic".

Using a JavaScript framework like Vue.js means your JavaScript code will be more organized, easier to read and maintain, and can be reused across projects. This is possible because Vue.js, like many other modern JavaScript frameworks, uses components. These components are reusable pieces of code that represent parts of your web page.

So, in short, JavaScript makes your website interactive and responsive, and a framework like Vue.js gives you the tools and structure to make the development process more efficient and the code cleaner.

## Why Use Vue.js?

Vue.js is a powerful JavaScript framework specifically designed to build user interfaces, particularly single-page applications. Let's break down some reasons why you might choose Vue.js over others:

**Interactivity**: Vue.js lets you create web applications that react to user inputs. With Vue.js, you can build features like a live chat window or a feedback form that updates in real time.

**Reusability**: Vue.js allows you to create custom components that you can reuse across your application. This leads to less code, fewer bugs, and a more consistent user interface.

**Reactivity**: Vue.js uses a reactive data system. When the underlying data changes, the parts of the website that use this data automatically update.
Routing: Vue.js comes with vue-router, which lets you switch between different parts of your application without refreshing the page, creating a smoother user experience.

**Easy Integration**: Vue.js can be incrementally adopted, meaning you can add it to an existing project and start benefiting from its features without needing to rewrite your existing code.

**Developer Experience**: Vue.js is designed to be easy to learn and use, with a simple API and guide, and great developer tools.

A Vue.js application is typically made up of a tree of components, where parent components pass data down to child components via props, and child components emit events up to the parent components when something happens (like a user clicking a button). By using Vue.js, your web application will be more organized, more maintainable, and offer a better user experience.

## Components

In Vue.js, components are one of the core concepts you need to understand. A component is essentially a reusable instance with a name. We can liken components to Lego blocks: individually, they may not look like much, but combined in the right way, they can create intricate, complex structures.

A Vue component is a custom, reusable HTML element that encapsulates its own functionality and styling. This means that a component has its own template (HTML), logic (JavaScript), and styling (CSS).

Think of a component as a mini-application with its own logic and presentation that you can reuse throughout your app. For instance, you might have a "Button" component, a "Navbar" component, or a "UserProfile" component. Once you've defined these components, you can reuse them wherever you need that specific functionality.

The main advantage of components is reusability. By encapsulating functionality within components, you avoid duplicating code. If you want to change how a component works, you only need to update it in one place, and those changes will propagate to every instance of the component.

This not only makes your codebase easier to maintain but also enhances consistency across your application. If you decide to change the look of your buttons, you only need to update the "Button" component, and all the buttons across your application will be updated.

## Breaking Our Static Site Into Components
In the context of our static HTML and CSS website, we can identify the following components, each of which encapsulates specific functionality and can be reused as needed. Identifying these components will significantly reduce code duplication and improve the maintainability of the website as it evolves:

**Header**: The topmost part of the site, containing the site's logo and the shopping cart. It's a component you're likely to use on every page of your site.
- **Navigation**: A subcomponent of the Header. This encapsulates the navigation links, allowing users to move between different sections or pages of the site.
- **Slider**: An image carousel/slider component, often found in the Hero section of a site. This component can showcase multiple images or banners in a rotating fashion.

**NewArrival**: A component that displays the newly arrived products. This can be useful on e-commerce or retail sites to highlight new products.
- **ProductCard**: A subcomponent of the NewArrival section. It represents each individual product, encapsulating product details like image, name, and price.
  
**Review**: A component showcasing customer reviews. A crucial part of e-commerce and service-oriented sites where customer feedback is displayed.
- **ReviewCard**: A subcomponent of the Review section. It represents each individual review, encapsulating the reviewer's name, rating, and comments.
  
**Services**: A component displaying the various services the site offers. Each service is presented in a consistent, clear format.
- **ServiceCard**: A subcomponent of the Services section. Each ServiceCard represents a specific service, providing details like service name, description, and perhaps an associated icon or image.
  
**LoginForm**: A standalone component representing a user login form. It encapsulates fields like username and password and possibly options for social login or forgot password.

**Footer**: The footer of the page, containing various information and links. It's a standard component for virtually every website.
- **Contact**: A subcomponent of the Footer. It represents the contact information section, typically containing email, phone number, and address.
- **GetHelp**: A subcomponent of the Footer. This section provides help-related links, such as FAQs, return policy, or customer support.
- **OurStores**: A subcomponent of the Footer. It represents a section displaying physical store locations if applicable.
- **Newsletter**: A subcomponent of the Footer. This section allows users to subscribe to the site's newsletter, fostering ongoing engagement.
  
By breaking down our static HTML site into these reusable components, we ensure that each piece of functionality is encapsulated, maintainable, and easy to manage. If we need to change the appearance or functionality of one of these components, we only have to make the change in one place. This approach promotes consistency across the site, reduces the likelihood of errors, and makes the code easier to understand and work with.

## Installation / Setting up a vue project 
<blockquote>
Node Version Requirement

Vue CLI 4.x requires Node.js version 8.9 or above (v10+ recommended). 
</blockquote>

#### To install Vue CLI: 

```bash
npm install -g @vue/cli
```

#### To verify installation 

```bash
vue --version
```

#### To create new project
```bash
vue create shoes-frontend
```

In the setup it will ask you which version of vue do you want, Select vue 2. if you `cd` into the project directory and run `yarn serve` you will be prompted wih a url, if you visit the URL in the browser you should see: 
<img width="704" alt="Screenshot 2023-07-15 at 15 00 39" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/0aa18f9b-e4df-42f1-b41b-9c637a65d3da">
<img width="710" alt="Screenshot 2023-07-15 at 15 01 06" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/e817ed70-6e56-4007-934b-5a54bb20bd63">
<img width="1308" alt="Screenshot 2023-07-15 at 15 02 03" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/a00a7916-5969-48fe-b818-283f1115800a">




