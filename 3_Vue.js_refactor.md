# Vue.js Refactor

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

**About**: A component that displays the about section
  
**Review**: A component showcasing customer reviews. A crucial part of e-commerce and service-oriented sites where customer feedback is displayed.
- **ReviewCard**: A subcomponent of the Review section. It represents each individual review, encapsulating the reviewer's name, rating, and comments.
  
**Services**: A component displaying the various services the site offers. Each service is presented in a consistent, clear format.
- **ServiceCard**: A subcomponent of the Services section. Each ServiceCard represents a specific service, providing details like service name, description, and perhaps an associated icon or image.
  
**LoginForm**: A standalone component representing a user login form. It encapsulates fields like username and password and possibly options for social login or forgot password.

**Footer**: The footer of the page, containing various information and links. It's a standard component for virtually every website.
  
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

In the setup it will ask you which version of vue do you want, Select vue 2. if you `cd` into the project directory and run `yarn serve` you will be prompted wih a url

Move `bg1.png` into `shoes-frontend/src/assets`

## Creating our components 
open up `shoes-frontend` in your code editor 

Within the src/components directory, create the following files:

**Header.vue**: This file will contain the component for the site's header, including the logo and shopping cart.

**Navigation.vue**: This file will contain the component for the navigation links.

**Slider.vue**: This file will contain the component for the image carousel/slider.

**NewArrival.vue**: This file will contain the component for displaying newly arrived products.

**ProductCard.vue**: This file will contain the component for each individual product within the NewArrival section.

**About.vue**: This file will contain the component for the about section.

**Review.vue**: This file will contain the component for showcasing customer reviews.

**ReviewCard.vue**: This file will contain the component for each individual review within the Review section.

**Services.vue**: This file will contain the component for displaying the site's services.

**ServiceCard.vue**: This file will contain the component for each individual service within the Services section.

**LoginForm.vue**: This file will contain the component for the login form.

**Footer.vue**: This file will contain the component for the footer of the page.

Please ensure each of these files is created with the .vue extension, as this is the standard file extension for Vue.js single-file components.

## App.vue
`App.vue` serves as the root component of your Vue.js application. It is typically the first component to be loaded and renders all other components within it. In other words, it is the parent component for all other components in your Vue application.

Lets update our `App.vue` to include all of our newly created components:

```vue
<template>
  <div id="app">
    <Header />
    <NewArrival />
    <About />
    <Review />
    <Services />
    <LoginForm />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import NewArrival from './components/NewArrival.vue';
import Review from './components/About.vue';
import Review from './components/Review.vue';
import Services from './components/Services.vue';
import LoginForm from './components/LoginForm.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    NewArrival,
    About,
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
<img width="1684" alt="Screenshot 2023-07-15 at 20 13 52" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/9088bc4b-affe-49e6-8d3d-730227917724">

## NewArival.vue
In your Header.vue, enter:
```vue
<template>
    <div class="products" id="Products">
      <h1>Products</h1>
      <div class="box">
        <ProductCard v-for="product in products" :key="product.id" :product="product"/>
      </div>
    </div>
  </template>
  
  <script>
  import ProductCard from './ProductCard.vue';
  
  export default {
    components: {
      ProductCard
    },
    data() {
      return {
        products: [
          {
            id: 1,
            image: "image/shoes1.png",
            name: "NIKE",
            description: "Lorem ipsum dolor sit, amet consectetur adipisicing elit.",
            price: "$100.99",
            stars: {
              full: 5,
              half: 0,
              empty: 0
            }
          },
          {
            id: 2,
            image: "image/shoes2.png",
            name: "NIKE",
            description: "Lorem ipsum dolor sit, amet consectetur adipisicing elit.",
            price: "$110.99",
            stars: {
              full: 5,
              half: 0,
              empty: 0
            }
          },
        ]
      }
    }
  }
  </script>
  
  <style scoped>
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
  </style>
```
In your `ProductCard.vue` enter:
```vue
<template>
    <div class="card">
      <div class="image">
        <img :src="product.image">
      </div>
      <div class="products_text">
        <h2>{{ product.name }}</h2>
        <p>
          {{ product.description }}
        </p>
        <h3>{{ product.price }}</h3>
        <div class="products_star">
          <i class="fa-solid fa-star" v-for="i in product.stars.full" :key="i"></i>
          <i class="fa-solid fa-star-half-stroke" v-if="product.stars.half"></i>
          <i class="fa-regular fa-star" v-for="i in product.stars.empty" :key="i"></i>
        </div>
        <a href="#" class="btn">Add To Cart</a>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      product: {
        type: Object,
        required: true,
      },
    },
  };
  </script>
  
  <style scoped>
  .card {
    width: 290px;
    height: 440px;
    box-shadow: 0 0 8px #6c14d0;
    border-radius: 5px;
    text-align: center;
    padding: 10px 20px;
    background: #f6f6f6;
  }
  
  .card .image {
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .card .image img {
    width: 150px;
    margin: 15px 0;
    transition: 0.3s;
  }
  
  .card .products_text h2 {
    font-size: 30px;
    margin-top: 15px;
  }
  
  .card .products_text p {
    color: #91919191;
    line-height: 21px;
    margin: 8px 0;
  }
  
  .card .products_text h3 {
    margin: 7px 0;
  }
  
  .card .products_text .products_star {
    color: orange;
    margin-bottom: 19px;
    cursor: pointer;
  }
  
  .card .products_text .btn {
    text-decoration: none;
    padding: 10px 20px;
    background: linear-gradient(to right, #c72092 , #6c14d0);
    color: white;
  }
  </style>
```

Lets break this down: 

**in `NewArival.vue` we define a `data()`**: In Vue.js, the `data()` function is a special function used in components to define and initialize the data properties used within that component. It is a key part of the Vue instance and plays a crucial role in managing the component's data. We set a prop `products` equal to an array of Product objects each containing attributes such as name and description. We give each a unique  `id` so that we can differentiate each one when it comes to looping through them

**in `NewArival.vue` we do `v-for`**: The v-for directive is a powerful feature in Vue.js that allows you to iterate over a collection or an array of items and render a template or component for each item. It provides a convenient way to generate repetitive content dynamically. No more re-writing the same content over and over like we had to in the static site! 🔥

**in `NewArival.vue` we do :product="product"`**: This is how we pass the product data to the ProductCard component as a prop. The :product syntax (or v-bind:product) is used to bind the product variable to the product prop of the ProductCard component. By passing the product as a prop, we make the data accessible within the ProductCard component and can use it to display information specific to each product.

then in `ProductCard.vue` we accept the incoming data being passed in from `NewArival.vue` with 

```vue
    props: {
      product: {
        type: Object,
        required: true,
      },
```

we can now use that incoming data within `ProductCard` like `<h2>{{ product.name }}</h2>`

If we take a look at the result in the browser we should now see: 

<img width="1685" alt="Screenshot 2023-07-15 at 20 14 14" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/361d5abd-e6e3-4cf6-9feb-aba405dac9c1">


## About.vue
In your About.vue, enter:
```vue
<template>
    <div class="about" id="About">
        <h1>Web<span>About</span></h1>

        <div class="about-main">
            <div class="about-image">
                <div class="about-small-image">
                    <img v-for="image in images" :src="image.src" @click="updateMainImage(image.src)" :key="image.id">
                </div>

                <div class="image-container">
                    <img :src="selectedImage || defaultImage" id="imagebox">
                </div>
            </div>

            <div class="about-text">
                <p>
                    Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical
                    Latin
                    literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at
                    Hampden-Sydney
                    College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum
                    passage,
                    and going through the cites of the word in classical literature, discovered the undoubtable source.
                    Lorem
                    Ipsum comes from sections 1.10.32 and 1.10.33 of "de Finibus Bonorum et Malorum" (The Extremes of Good
                    and
                    Evil) by Cicero, written in 45 BC. This book is a treatise on the theory of ethics, very popular during
                    the
                    Renaissance. The first line of Lorem Ipsum, "Lorem ipsum dolor sit amet..", comes from a line in section
                    1.10.32. The standard chunk of Lorem Ipsum used since the 1500s is reproduced below for those
                    interested.
                    Sections 1.10.32 and 1.10.33 from "de Finibus Bonorum et Malorum" by Cicero are also reproduced in their
                    exact original form, accompanied by English versions from the 1914 translation by H. Rackham.
                </p>
            </div>
        </div>

        <a href="#" class="about-btn">Shop Now</a>
    </div>
</template>
  
<script>
export default {
    name: 'About',
    data() {
        return {
            selectedImage: '',
            images: [
                { id: 1, src: 'image/red_shoes1.png' },
                { id: 2, src: 'image/red_shoes2.png' },
                { id: 3, src: 'image/red_shoes3.png' },
                { id: 4, src: 'image/red_shoes4.png' }
            ],
            defaultImage: 'image/red_shoes1.png'
        };
    },
    methods: {
        updateMainImage(src) {
            this.selectedImage = src;
        }
    }
}
</script>
  
<style>
.about {
    width: 100%;
    height: 100vh;
    padding: 35px 0;
}

.about h1 {
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

.about h1 span {
    background: linear-gradient(to right, #c72092, #6c14d0);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-left: 15px;
}

.about-main {
    position: relative;
    top: 40%;
    left: 50%;
    transform: translate(-50%, -50%);
    display: flex;
    justify-content: space-around;
    align-items: center;
}

.about-image {
    display: flex;
    margin-top: 50px;
}

.about-image .about-small-image {
    display: flex;
    flex-direction: column;
    position: relative;
    top: 15px;
}

.about-image .about-small-image img {
    height: 92px;
    margin: 5px 0;
    cursor: pointer;
    background: linear-gradient(to right, #6c14d0, #c72092);
    display: block;
    border-radius: 6px;
    padding: 5px 5px;
    box-shadow: 0 0 6px rgba(0, 0, 0, 0.6);
    opacity: 0.8;
    transition: 0.3s;
}

.about-image .about-small-image img:hover {
    opacity: 1;
}

.about-image .image-container {
    padding: 10px;
    display: flex;
}

.about-image .image-container img {
    border: 3px solid #6c14d0;
    border-radius: 20px;
    height: 430px;
    padding: 30px;
    box-shadow: 0 0 8px #6c14d0;
}

.about-text {
    margin-top: 45px;
}

.about-text p {
    background: linear-gradient(to left, #c72092, #6c14d0);
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

.about-btn {
    color: black;
    background: none;
    position: relative;
    top: 10%;
    left: 50%;
    transform: translate(-50%, -50%);
    padding: 10px 25px;
    border: 2px solid #c72092;
    text-decoration: none;
    box-shadow: 0 0 8px #c72092;
    transition: 0.5s;
}

.about-btn:hover {
    border: 2px solid transparent;
    background: #c72092;
    color: white;
}</style>
```

Let's break down the new stuff: 

In Vue.js, methods are functions that are defined within a Vue component and can be called to perform certain actions or operations. They provide a way to define custom behavior and logic within the component.

Methods in Vue.js are typically defined within the methods property of the component's options object. Here's an example:

```vue
<script>
export default {
  name: 'MyComponent',
  data() {
    return {
      message: 'Hello, Vue!'
    };
  },
  methods: {
    greet() {
      console.log(this.message);
    }
  }
}
</script>
```

In this example, we have a component named MyComponent with a data property containing a message variable. The methods property defines a greet method that logs the value of this.message to the console.

Methods can be invoked from within the component's template or from other methods using the this keyword. Here's how you can call the greet method from the template:

```vue
<template>
  <div>
    <button @click="greet">Greet</button>
  </div>
</template>
```

When the button is clicked, the greet method will be executed, and the message will be logged to the console.

Methods can also accept parameters if needed. You can pass data from the template or other methods as arguments to a method:

```vue
<script>
export default {
  name: 'MyComponent',
  methods: {
    sayHello(name) {
      console.log(`Hello, ${name}!`);
    }
  }
}
</script>
```
Then, you can call the sayHello method with an argument from the template:

```vue
<template>
  <div>
    <button @click="sayHello('John')">Say Hello</button>
  </div>
</template>
```

In this case, clicking the button will invoke the sayHello method with the argument 'John', resulting in the message "Hello, John!" being logged to the console.

Methods are a fundamental part of Vue.js components and allow you to define custom behavior, handle events, perform computations, make API calls, and more. They provide the flexibility to add interactivity and dynamic functionality to your Vue applications.

If we look in the browser at the result we should now see: 

<img width="1690" alt="Screenshot 2023-07-15 at 20 14 40" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/834dd218-21a9-452d-aa10-1cf588589d2d">


## Review.vue
In your Review.vue, enter:
```vue
<template>
  <div class="reviews">
    <h1>Reviews</h1>
    <div class="review-list">
      <ReviewCard v-for="review in reviews" :key="review.id" :review="review" />
    </div>
  </div>
</template>

<script>
import ReviewCard from './ReviewCard.vue';

export default {
  name: 'Review',
  components: {
    ReviewCard
  },
  data() {
    return {
      reviews: [
        {
          id: 1,
          title: 'Great Product',
          content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
          rating: [1, 1, 1, 1, 0.5]
        },
        {
          id: 2,
          title: 'Excellent Quality',
          content: 'Vivamus et massa dictum, interdum nibh at, efficitur odio.',
          rating: [1, 1, 1, 1, 1]
        }
      ]
    };
  }
}
</script>

<style>
/* Styles for the reviews component */
.reviews {
  width: 100%;
  height: 100vh;
  padding-top: 80px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #f5f5f5;
}

.reviews h1 {
  font-size: 48px;
  font-weight: bold;
  margin-bottom: 30px;
  text-transform: uppercase;
  background: linear-gradient(to right, #c72092, #6c14d0);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.review-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
  gap: 20px;
  justify-items: center;
  align-items: flex-start;
}
</style>
```

In your ReviewCard.vue, enter:
```vue
<template>
    <div class="review-card">
      <h2>{{ review.title }}</h2>
      <p>{{ review.content }}</p>
      <div class="rating">
        <span v-for="star in review.rating" :key="star" class="star"></span>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ReviewCard',
    props: ['review']
  }
  </script>
  
  <style>
  .review-card {
    width: 500px;
    background: #f3f1f1;
    padding: 20px 25px;
    border-radius: 5px;
    margin: 15px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
  }
  
  .review-card h2 {
    font-size: 24px;
    margin-bottom: 10px;
  }
  
  .review-card p {
    font-size: 16px;
    line-height: 1.5;
    margin-bottom: 20px;
  }
  
  .review-card .rating {
    color: orange;
    margin-bottom: 10px;
  }
  
  .review-card .star {
    display: inline-block;
    width: 20px;
    height: 20px;
    background-color: orange;
    border-radius: 50%;
    margin-right: 5px;
  }
  </style>
```

This is a similar setup to `NewArival` and `Product` there are no new concepts to learn here 🚀

If we check this out in the browser now we should see: 

<img width="1683" alt="Screenshot 2023-07-15 at 20 14 57" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/24e24f7d-6040-4536-b7da-e646ce735ba3">


## Services.vue
In your Services.vue, enter:
```vue
<template>
    <div class="services">
      <h1>Our Services</h1>
      <div class="services-cards">
        <ServiceCard v-for="service in services" :key="service.id" :service="service" />
      </div>
    </div>
  </template>
  
  <script>
  import ServiceCard from './ServiceCard.vue';
  
  export default {
    name: 'Service',
    components: {
      ServiceCard
    },
    data() {
      return {
        services: [
          {
            id: 1,
            title: 'Service 1',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.',
            icon: 'fa-cog'
          },
          {
            id: 2,
            title: 'Service 2',
            description: 'Vivamus et massa dictum, interdum nibh at, efficitur odio.',
            icon: 'fa-wrench'
          }
        ]
      };
    }
  }
  </script>
  
  <style>
  .services {
    width: 70%;
    margin: 0 auto;
    text-align: center;
    padding: 80px 0 10px 0;
  }
  
  .services h1 {
    font-size: 60px;
    text-transform: uppercase;
    background: linear-gradient(to left, #c72092, #6c14d0);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  
  .services .services-cards {
    width: 80%;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: relative;
    top: 50px;
  }
  </style>
```

In your ServiceCard.vue, enter:
```vue
<template>
    <div class="service-card">
      <i class="service-icon" :class="iconClass"></i>
      <h3>{{ service.title }}</h3>
      <p>{{ service.description }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ServiceCard',
    props: ['service'],
    computed: {
      iconClass() {
        return 'fas fa-' + this.service.icon;
      }
    }
  }
  </script>
  
  <style>
  .service-card {
    width: 300px;
    margin: 0 auto;
    text-align: center;
  }
  
  .service-card .service-icon {
    font-size: 60px;
    color: orange;
    margin: 20px 0;
    cursor: pointer;
  }
  
  .service-card h3 {
    margin-bottom: 12px;
    font-size: 19px;
  }
  
  .service-card p {
    text-align: center;
    color: #919191;
    margin-bottom: 60px;
  }
  </style>
```

Let's explain the new stuff: 

**Computed**: In our application, we have a list of services displayed on the Services page. Each service has an icon associated with it. We want to dynamically generate the CSS class for each icon based on the icon property of the service object.

To achieve this, we can use a computed property. Think of a computed property as a helper that automatically calculates and provides us with the appropriate icon class whenever we need it.

So, we define a computed property called iconClass in the ServiceCard.vue component. Inside the iconClass computed property, we write a function that determines the icon class based on the icon property of the service.

For example, if the icon property is set to "shopping-cart", the iconClass computed property will return the CSS class name "fas fa-shopping-cart". If the icon property is `"heart"`, the computed property will return `"fas fa-heart"`.

We can then use this computed property in the template of ServiceCard.vue. Instead of hardcoding the CSS class for the icon, we simply use iconClass in the template. Vue will automatically calculate the appropriate icon class based on the icon property of the service.

This way, we can easily change the icon for each service by updating the icon property, and the computed property will take care of generating the correct CSS class for us. It keeps our template clean and allows us to reuse the computed logic throughout the component.

So, in summary, computed properties are like handy helpers that calculate and provide us with derived values based on existing data properties. They help us simplify our code, make it more maintainable, and keep our templates clean by encapsulating the logic for derived values separately.

If we take a look at the result in our browser we should see: 

<img width="1690" alt="Screenshot 2023-07-15 at 20 15 17" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/23f0dc7a-2ab2-4d5e-9cb1-87c29961180b">


## LoginForm.vue
In your LoginForm.vue, enter:
```vue
<template>
    <div class="login-form">
      <div class="left">
        <img src="image/logshoes.png">
      </div>
  
      <div class="right">
        <h1>Welcome Back!</h1>
  
        <form @submit="submitForm">
          <p>User Name</p>
          <div class="user">
            <i class="fa-solid fa-user"></i>
            <input v-model="username" type="text" name="user" placeholder="User Name" class="username">
          </div>
  
          <p class="password-tag">Password</p>
          <div class="password">
            <i class="fa-solid fa-lock"></i>
            <input v-model="password" type="password" name="password" placeholder="Password">
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
  </template>
  
  <script>
  export default {
    name: 'LoginForm',
    data() {
      return {
        username: '',
        password: ''
      };
    },
    methods: {
      submitForm() {
        // Handle form submission logic here
        // You can access the form values using this.username and this.password
      }
    }
  }
  </script>
  
  <style scoped>
  .login-form {
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: space-around;
    align-items: center;
    background-image: url(/public/image/loging_bg.png);
    background-size: cover;
    background-position: center;
  }
  
  .login-form .left img {
    width: 650px;
  }
  
  .login-form .right {
    position: relative;
    top: -50px;
    left: -60px;
    padding: 50px 80px;
  }
  
  .login-form .right h1 {
    font-family: prevattscriptssk;
    font-size: 45px;
    margin-bottom: 40px;
  }
  
  .login-form .right p {
    margin-bottom: 5px;
  }
  
  .login-form .right .user {
    border: 2px solid #6c14d0;
    border-radius: 5px;
    width: 350px;
    height: 40px;
    display: flex;
  }
  
  .login-form .right .user i {
    position: relative;
    top: 9px;
    left: 15px;
    color: #c72092;
  }
  
  .login-form .right .user .username {
    position: relative;
    left: 9%;
    width: 295px;
    background: none;
    outline: none;
    border: none;
    display: flex;
    font-size: 15px;
  }
  
  .login-form .right .password-tag {
    margin: 15px 0 5px 0;
  }
  
  .login-form .right .password {
    border: 2px solid #6c14d0;
    border-radius: 5px;
    width: 350px;
    height: 40px;
    display: flex;
  }
  
  .login-form .right .password i {
    position: relative;
    top: 9px;
    left: 15px;
    color: #c72092;
  }
  
  .login-form .right .password input {
    position: relative;
    left: 9%;
    width: 295px;
    background: none;
    border: none;
    outline: none;
    display: flex;
    font-size: 15px;
  }
  
  ::-webkit-input-placeholder {
    color: black;
    opacity: 0.7;
  }
  
  .login-form .right .forget {
    position: relative;
    left: 60%;
    margin: 6px 0 10px 0;
    cursor: pointer;
  }
  
  .login-form .right button {
    width: 350px;
    color: white;
    padding: 7px 20px;
    border: none;
    border-radius: 5px;
    font-size: 20px;
    cursor: pointer;
    background: linear-gradient(to right, #c72092 , #6c14d0);
  }
  
  .login-form .right .loging-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 25px;
  }
  
  .login-form .right .loging-icon a {
    width: 30px;
    height: 30px;
    margin: 0 2px;
    border-radius: 50%;
    background: #f3f3f3;
    box-shadow: 0 0 5px rgba(0,0,0,0.6);
  }
  
  .login-form .right .loging-icon img {
    width: 20px;
    margin: 5px 5px;
  }
  </style>
```

Let's explain the new stuff: 

**`v-model`**:  the v-model directive is used for two-way data binding between form input elements and the component's data. It allows you to automatically sync the data between the form inputs and the component's data properties.

When you use v-model on an input element, such as v-model="username", it creates a connection between the input value and the username data property. Any changes made in the input element will be automatically reflected in the username property, and vice versa.

In the LoginForm.vue component, we have two input fields: one for the username and one for the password. We bind these input fields to the component's data using v-model.

For example, in the username input field:

```vue
<input v-model="username" type="text" name="user" placeholder="User Name" class="username">
```

Here, the v-model="username" binds the input value to the username data property. So, whenever the user types something in the input field, the username property in the component will be updated automatically.

Similarly, we bind the password input field to the password data property:

```vue
<input v-model="password" type="password" name="password" placeholder="Password">
```

By using v-model, you eliminate the need for manually handling the input and change events and updating the data properties yourself. Vue.js takes care of synchronizing the input values and the component's data for you.

In the component's data section, you will see:

```vue
data() {
  return {
    username: '',
    password: ''
  };
},
```

These username and password data properties will store the values entered by the user in the corresponding input fields. You can access these values in the submitForm method or any other methods in the component.

This way, Vue.js simplifies form handling by providing a convenient way to bind form inputs to data properties and keep them in sync automatically.

If we now check in our browser we should see: 

<img width="1666" alt="Screenshot 2023-07-15 at 20 15 40" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/729b384d-81fb-4f16-929d-46c221d1d03e">


## Footer.vue
In your Footer.vue, enter:
```vue
<template>
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
            <input type="text" placeholder="Your email here">
            <button type="submit">Subscribe</button>
          </div>
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'Footer',
  };
  </script>
  
  <style>
  /* Styles for the footer component */
  footer {
    width: 100%;
  }
  
  .footer_main {
    width: 100%;
    background: #f3f1f1;
    display: flex;
    justify-content: space-around;
  }
  
  .tag {
    margin: 10px 0;
  }
  
  .tag .center {
    text-align: center;
  }
  
  .tag h1 {
    font-size: 25px;
    margin: 25px 0;
    color: #1c0080;
  }
  
  .tag a {
    display: block;
    color: black;
    text-decoration: none;
    margin: 9px 0;
  }
  
  .tag a i {
    padding: 0 10px;
    transition: 0.3s;
  }
  
  .tag a i:hover {
    color: #c72092;
  }
  
  .tag .social_link {
    display: flex;
  }
  
  .tag .social_link a {
    width: 30px;
    height: 30px;
    border-radius: 50%;
    text-align: center;
    text-decoration: none;
    color: black;
    box-shadow: 0 0 20px 10px rgba(0, 0, 0, 0.05);
    position: relative;
    margin: 0 5px;
    z-index: 10;
    overflow: hidden;
  }
  
  .tag .social_link a .fa-brands {
    font-size: 15px;
    line-height: 30px;
    z-index: 10;
    position: relative;
    transition: 0.5s;
  }
  
  .tag .social_link a:hover i {
    color: white;
  }
  
  .tag .social_link a::after {
    content: "";
    width: 100%;
    height: 100%;
    top: 0;
    left: -90px;
    background: linear-gradient(-45deg, #c72092, #6c14d0);
    position: absolute;
    z-index: -10;
    transition: 0.5s;
  }
  
  .tag .social_link a:hover::after {
    left: 0;
  }
  
  .tag .search_bar {
    width: 230px;
    height: 30px;
    background: rgb(202, 202, 202);
    border-radius: 25px;
  }
  
  .tag .search_bar input {
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
  
  .tag .search_bar button {
    padding: 7px 15px;
    background: linear-gradient(to right, #c72092, #6c14d0);
    border: none;
    margin-top: 15px;
    border-radius: 25px;
    color: white;
    cursor: pointer;
  }
  </style>
```

No new concepts have been introduced here 🙌🏻

If we check what the result is in our browser we should see:

<img width="1660" alt="Screenshot 2023-07-15 at 20 15 56" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/636ee27e-d2e2-4207-a017-8706e3b756c4">


## Congratulations
Well done! you made it through this section. I hope you now understand how breaking our website into small usable components helps us. I also hope you now understand some of the value vue.js brings us. There is alot more to learn in terms of vue.js but throughout this project I have shown you the very basics. We now have a beautiful vue.js application utalising components and data. In the next section we will move that data into a `database` and retrieve it using an `API` which we will build together using the `Laravel` framework

# Ready for the next section? 
[lets go!](https://github.com/michaelbarley/new-starter-demo-project/blob/main/4_laravel_API.md)
