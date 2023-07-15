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

In the newly created project folder, copy the `image` folder from the Static HTML and CSS project and place it within shoes-frontend/public

<img width="244" alt="Screenshot 2023-07-15 at 17 54 30" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/5e915ddc-f93f-4cd8-bf06-85e05fe56c17">

In the setup it will ask you which version of vue do you want, Select vue 2. if you `cd` into the project directory and run `yarn serve` you will be prompted wih a url, if you visit the URL in the browser you should see: 

<img width="1308" alt="Screenshot 2023-07-15 at 15 02 03" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/a00a7916-5969-48fe-b818-283f1115800a">

Move `bg1.png` into `shoes-frontend/src/assets`

<img width="250" alt="Screenshot 2023-07-15 at 18 00 55" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/8d853369-ef81-424f-ae9c-12e5d2ee0dd2">

## Creating our components 
open up `shoes-frontend` in your code editor 

Within the src/components directory, create the following files:

**Header.vue**: This file will contain the component for the site's header, including the logo and shopping cart.

**Navigation.vue**: This file will contain the component for the navigation links.

**Slider.vue**: This file will contain the component for the image carousel/slider.

**NewArrival.vue**: This file will contain the component for displaying newly arrived products.

**ProductCard.vue**: This file will contain the component for each individual product within the NewArrival section.

**Review.vue**: This file will contain the component for showcasing customer reviews.

**ReviewCard.vue**: This file will contain the component for each individual review within the Review section.

**Services.vue**: This file will contain the component for displaying the site's services.

**ServiceCard.vue**: This file will contain the component for each individual service within the Services section.

**LoginForm.vue**: This file will contain the component for the login form.

**Footer.vue**: This file will contain the component for the footer of the page.

**Contact.vue**: This file will contain the component for the contact information section of the Footer.

**GetHelp.vue**: This file will contain the component for the help-related links section of the Footer.

**OurStores.vue**: This file will contain the component for the store locations section of the Footer.

**Newsletter.vue**: This file will contain the component for the newsletter subscription section of the Footer.

Please ensure each of these files is created with the .vue extension, as this is the standard file extension for Vue.js single-file components.

## App.vue
`App.vue` serves as the root component of your Vue.js application. It is typically the first component to be loaded and renders all other components within it. In other words, it is the parent component for all other components in your Vue application.

Lets update our `App.vue` to include all of our newly created components:

```vue
<template>
  <div id="app">
    <Header />
    <NewArrival />
    <Review />
    <Services />
    <LoginForm />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import NewArrival from './components/NewArrival.vue';
import Review from './components/Review.vue';
import Services from './components/Services.vue';
import LoginForm from './components/LoginForm.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    NewArrival,
    Review,
    Services,
    LoginForm,
    Footer
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

```

let's break this down piece by piece.

Vue Component Structure: 
A Vue component file usually consists of three parts: `<template>`, `<script>` and `<style>`.

**`<template>`** is where you write the HTML that this component will render.

**`<script>`** is where you write the JavaScript that controls the behavior of this component.

**`<style>`** is where you write the CSS that styles your component.
  
**`<template>`** section: The template in App.vue specifies what will be displayed when this component is used. In this case, it is a `<div>` element with an id of app, containing a series of other components: Header, NewArrival, Review, Services, LoginForm, and Footer. These components represent different sections of your application.

**`<script>`** section: The script part of App.vue does two main things:
- First, it imports the necessary components from their respective files using import statements. This makes the components available to be used within this file.
  
- Second, it exports a JavaScript object which configures the Vue component. The name field assigns a name to this component, and the components field registers the imported components so they can be used in the template.
  
**`<style>` section**: The style section provides CSS for the App component.
Styles defined here are global by default, meaning they can apply to HTML across your whole app.
In the example, the CSS rules are applied to the `#app` id, affecting the text font, color, and other styling properties within the div element with the app id.

**Vue Component Naming**: Components in Vue.js are given in PascalCase by convention, but when used in the DOM they should be in kebab-case. For example, NewArrival in JavaScript becomes `<new-arrival>` in HTML.

**Scoped and Global CSS**: CSS in Vue components is global by default, but you can make it apply only to the current component by adding the scoped attribute to the style tag (<style scoped>). The CSS rules within a scoped style tag won't leak out to other components, making it easier to avoid unintended side effects.

The `App.vue` file is a central piece of your application. It imports and integrates the other components to form the complete web application. Understanding its structure and purpose is key to mastering Vue.js development

## Header.vue
In your Header.vue, enter:

```vue
<template>
    <section>
      <Navigation />
      <Slider />
    </section>
  </template>
  
  <script>
  import Navigation from './Navigation.vue';
  import Slider from './Slider.vue';
  
  export default {
    name: 'Header',
    components: {
      Navigation,
      Slider
    }
  }
  </script>
  
  <style scoped>
  /* As there are no shared styles, this section can be left empty */
  </style>
```

In your `Navigation.vue`, enter:
```vue
<template>
    <nav>
      <div class="logo">
        <h1>Shoe<span>s</span></h1>
      </div>
      <ul>
        <li><a href="#Home">Home</a></li>
        <li><a href="#Products">Products</a></li>
        <li><a href="#About">About</a></li>
        <li><a href="#Review">Review</a></li>
        <li><a href="#Services">Services</a></li>
      </ul>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'Navigation',
  }
  </script>
  
  <style scoped>
  nav{
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
  
  nav .logo{
      font-size: 35px;
      color: #c72092;
      margin: 5px 0;
      cursor: pointer;
      position: relative;
      left: -4%;
  }
  
  nav .logo span{
      color: #6c14d0;
      text-decoration: underline;
  }
  
  nav ul{
      list-style: none;
  }
  
  nav ul li{
      display: inline-block;
      margin: 5px 15px;
  }
  
  nav ul li a{
      text-decoration: none;
      color: black;
      transition: 0.2s;
  }
  
  nav ul li a:hover{
      color: #c72092;
  }
  
  nav .icons i{
      margin: 0 4px;
      cursor: pointer;
      font-size: 18px;
      transition: 0.3s;
  }
  
  nav .icons i:hover{
      color: #c72092;
  }
  </style>
```

In your `Slider.vue`, enter:
```vue
<template>
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
  </template>
  
  <script>
  export default {
    name: 'Slider',
  }
  </script>
  
  <style scoped>
  .main .main_content {
      display: flex;
      align-items: center;
      justify-content: space-around;
  }
  
  .main .main_content .main_text h1{
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
  
  .main .main_content .main_text h1 span{
      font-size: 70px;
      background: linear-gradient(to right, #c72092,#6c14d0);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
  }
  
  .main .main_content .main_text p{
      width: 600px;
      text-align: justify;
      line-height: 21px;
      position: relative;
      top: 85px;
      left: 5%;
  }
  
  .main .main_content .main_image img{
      width: 650px;
      position: relative;
      left: 20px;
      top: 75px;
  }
  
  .main .button{
      position: absolute;
      left: 6%;
      padding: 10px 20px;
      border-radius: 30px;
      background: linear-gradient(to right,#c72092 , #6c14d0);
  }
  
  .main .button a{
      color: white;
      text-decoration: none;
  }
  
  .main .button i{
      color: white;
      margin-left: 5px;
      transition: 0.3s;
  }
  
  .main .button:hover i{
      transform: translateX(6px);
  }
  </style>
```

As you can see, we are just chopping up our static HTML and CSS application, seperating the styles accross the components. You can also see here that `Header.vue` is the parent and contains `Navigation.vue` as well as `Slider.vue`. Therfore in `App.vue` when we import `Header.vue` we also see the Navigation and Slider. 

If we run `yarn serve` in the terminal and go to the url it generates you should see in the browser: 
<img width="1314" alt="Screenshot 2023-07-15 at 18 14 35" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/1b905e5c-db36-42fc-bdc9-bff5892c2f9e">














