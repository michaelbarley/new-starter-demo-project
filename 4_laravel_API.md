# Laravel_API
By the end of this section you will have a Laravel API communicating with our Vue.js application to retrieve data for Products

## Server Side
To understand server-side programming, let's start by discussing the two applications you've built so far: the static e-commerce site written in HTML and CSS and the Vue.js application.

**Static E-commerce Site**:
The static e-commerce site you created using HTML and CSS is a collection of web pages that don't interact with a server. These pages are pre-rendered and don't have dynamic functionality. While static sites can be simple and fast, they have limitations. For instance, you can't fetch real-time data, handle user logins, or process forms without involving a server. Any changes or updates to the site require manually editing the HTML and CSS files.

**Vue.js Application**:
The Vue.js application you built introduces interactivity and dynamic behavior. Vue.js is a JavaScript framework that allows you to create single-page applications (SPAs). SPAs load once, and then the content changes dynamically as users interact with the application. This approach is great for creating smooth and responsive user experiences. However, the Vue.js application you've built is still limited to the client-side, meaning it runs entirely on the user's device (browser) without communicating with a server.

Now, let's discuss the concept of server-side programming and the benefits it brings:

Server-side programming involves writing code that runs on the server rather than the client's device. This server-side code processes requests from clients, performs various tasks, and sends back responses. It enables dynamic behavior, data storage, and communication with databases. Server-side programming allows you to create more advanced and interactive applications. Here's why incorporating a server-side language like PHP with Laravel and a database is beneficial:

**Dynamic Content and Real-Time Updates**:
With server-side programming, you can generate dynamic content based on user requests. For example, an e-commerce site can display products from a database, handle user registrations, process payments, and update inventory in real-time. You can fetch data from a database, perform calculations, and generate personalized content on the fly.

**Data Storage and Management**:
A server-side language like PHP with Laravel allows you to connect your application to a database. A database is a structured way to store, organize, and retrieve data efficiently. By incorporating a database, you can store product information, user details, order history, and other relevant data. This enables persistent data storage, making your application more powerful and capable of handling large amounts of information.

**Security and Authentication**:
Server-side programming is crucial for implementing secure user authentication and authorization mechanisms. You can handle user logins, validate credentials, and control access to certain parts of your application. This ensures that only authorized users can perform specific actions, protecting sensitive data and maintaining the integrity of your application.

**Scalability and Code Reusability**:
By incorporating a server-side language and a framework like Laravel, you can write modular and reusable code. This makes it easier to scale and maintain your application as it grows. Laravel provides various tools, libraries, and conventions that simplify common tasks and help you follow best practices, reducing the complexity of building complex web applications.

In summary, incorporating a server-side language like PHP with Laravel and a database allows you to build powerful, dynamic, and interactive web applications. It enables real-time updates, data storage, security, authentication, and scalability. By understanding server-side programming concepts, you'll be able to develop more advanced applications and enhance your skills as a software engineer.

## Laravel
Laravel is a popular open-source PHP framework for building web applications. It provides a robust set of tools, libraries, and conventions that simplify the development process and promote good coding practices. Here's why we use Laravel for writing server-side code:

**MVC Architecture**:
Laravel follows the Model-View-Controller (MVC) architectural pattern. MVC separates different aspects of an application, making it more organized and maintainable. The Model represents data and database interactions, the View handles the presentation layer, and the Controller manages the application's logic and acts as an intermediary between the Model and View. This separation of concerns makes code more modular, reusable, and easier to understand.

**Routing and Request Handling**:
Laravel provides a powerful routing system that allows you to define clean and meaningful URLs for your application. With Laravel's routing, you can map URLs to specific actions or controllers, making it easier to handle incoming requests and direct them to the appropriate code. This helps in building clean and intuitive APIs and web applications.

**Database Abstraction and ORM**:
Laravel includes an intuitive and expressive Object-Relational Mapping (ORM) called Eloquent. Eloquent simplifies database interactions by providing a fluent and convenient syntax for working with databases. It allows you to define database tables as models and perform common database operations using a simple and readable syntax. Eloquent supports relationships, eager loading, query building, and many other advanced database features.

**Authentication and Security**:
Laravel provides built-in authentication and authorization mechanisms. It includes pre-built functionality for handling user registration, login, and password reset. Laravel's authentication system is highly customizable and secure, making it easier to implement user authentication and access control within your application. It helps in protecting user data, securing routes, and managing user sessions.

**Caching and Performance**:
Laravel offers built-in support for various caching systems, including popular options like Memcached and Redis. Caching helps improve the performance of your application by storing frequently accessed data in memory, reducing the need for repetitive database queries. Laravel's caching mechanisms are easy to use and allow you to cache different parts of your application, such as query results, views, or entire pages.

**Testing and Debugging**:
Laravel encourages and facilitates testing your application's code. It provides a robust testing framework that allows you to write unit tests, integration tests, and acceptance tests for your application. Laravel's testing tools help identify and fix issues early in the development process, ensuring a stable and reliable application. Additionally, Laravel has excellent error handling and logging mechanisms, making it easier to debug and troubleshoot your code.

**Ecosystem and Community**:
Laravel has a vibrant and active community of developers worldwide. It has a vast ecosystem of packages and extensions, allowing you to leverage existing solutions for common functionalities. Laravel's community actively contributes to its growth, regularly releasing updates, bug fixes, and new features. The extensive documentation, tutorials, and community support make it easier to learn and excel in Laravel development.

**Artisan**: 
Artisan is the command-line interface (CLI) included with Laravel, a popular PHP framework. It provides a set of helpful commands to assist with various development tasks, such as generating code, managing database migrations, running tests, and more.

Here are some key points about Artisan:

- Code Generation: Artisan allows you to generate boilerplate code for various components of your Laravel application, including controllers, models, migrations, commands, and more. This helps speed up the development process by providing a consistent structure and reducing the need for manual coding.
  
- Database Migrations: Artisan simplifies the management of database migrations in Laravel. Migrations are version control for your database schema, allowing you to create, modify, and roll back changes to the database structure. With Artisan commands, you can create migration files, run migrations to update the database, roll back migrations, and more.
  
- Task Automation: Artisan supports task automation through custom commands. You can create your own Artisan commands to automate repetitive tasks, schedule tasks to run at specific intervals using cron, and build command-line utilities specific to your application's requirements.
  
- Built-in Commands: Laravel ships with a wide range of pre-built Artisan commands. These commands cover a variety of tasks, such as running tests, clearing cache, optimizing the application, generating documentation, managing queues, and interacting with the application during development.
  
- CLI Testing: Artisan provides a testing environment within the command-line interface. This allows you to write and run tests for your application's functionality, ensuring that everything works as expected. Artisan's testing features make it easier to write and execute tests for commands, models, controllers, and other parts of your application.
  
- Extensibility: Artisan is designed to be extensible. You can create custom commands and add them to your application to perform specific tasks or integrate with external tools. This extensibility allows you to tailor Artisan to your project's unique requirements and automate any custom development workflows.

In summary, Laravel provides a powerful and comprehensive framework for writing server-side code using PHP. Its features such as the MVC architecture, routing system, database abstraction, authentication, caching, testing, and community support contribute to faster development, maintainable code, and secure and scalable web applications. Using Laravel can streamline your development process and enable you to build robust and feature-rich applications efficiently.

## Databases
A database is a structured collection of data that is organized, stored, and managed for efficient retrieval and manipulation. Databases are essential for applications that need to store and retrieve large amounts of data reliably and efficiently. Here's why databases can be useful:

**Persistent Data Storage**:
Unlike storing data in arrays or variables within your Vue.js project, databases provide a persistent and centralized storage solution. This means that the data stored in a database remains intact even if your application is restarted or the server experiences a power outage. By using a database, you can ensure the long-term availability and durability of your data.

**Scalability and Performance**:
Databases are designed to handle large amounts of data and provide efficient data retrieval mechanisms. When your e-commerce application grows and starts dealing with a substantial number of products, using a database allows you to scale your system without sacrificing performance. Databases can optimize data retrieval using indexes, caching, and query optimization techniques, resulting in faster response times.

**Structured Data Organization**:
Databases provide a structured way to organize and represent your data. Unlike storing products as arrays of objects in your Vue.js project, databases offer relational or non-relational data models. In a relational database, you can define tables and relationships between them, ensuring data consistency and enabling complex querying. This structured organization helps in managing and maintaining data integrity.

**Data Retrieval and Manipulation**:
Databases offer powerful querying capabilities that allow you to retrieve and manipulate data efficiently. You can use SQL (Structured Query Language) or other query languages specific to the database management system (DBMS) you choose. With queries, you can filter, sort, aggregate, and join data based on specific criteria. This makes it easier to fetch the relevant product information for displaying on your e-commerce site.

**Data Consistency and Integrity**:
Databases provide mechanisms to enforce data consistency and integrity rules. You can define constraints, such as uniqueness, data types, and foreign key relationships, to ensure that data adheres to specific rules. This helps in maintaining data quality and preventing inconsistencies or data corruption.

**Concurrent Data Access**:
When multiple users access your e-commerce application simultaneously, databases handle concurrent data access efficiently. They provide mechanisms like transactions and locking to ensure that data remains consistent and that multiple users can interact with the data without conflicts or data corruption.

**Security and Data Protection**:
Databases offer security features to protect your data from unauthorized access. You can define user roles, permissions, and access controls to ensure that only authorized individuals can read, modify, or delete data. Additionally, databases often provide backup and recovery mechanisms to safeguard your data against accidental loss or system failures.

**Data Analysis and Reporting**:
Databases can support advanced data analysis and reporting capabilities. By storing data in a structured format, you can leverage query tools, reporting frameworks, or business intelligence solutions to gain insights from your e-commerce data. This helps in making informed decisions, identifying trends, and optimizing business processes.

In summary, databases provide a reliable and efficient way to store and manage your e-commerce data. They offer persistent storage, scalability, structured organization, powerful querying, data consistency, security, and analysis capabilities. By transitioning from storing products as arrays in your Vue.js project to utilizing a database, you can improve data management, enhance scalability, and enable more advanced features and functionalities in your application.

## APIs
APIs (Application Programming Interfaces) are sets of rules, protocols, and tools that allow different software applications to communicate and interact with each other. APIs define how different software components can request and exchange data or perform specific actions. In the case of the Laravel API you're going to build, here's why it can be beneficial for your Vue.js application:

**Data Retrieval and Manipulation**:
The Laravel API you're creating will allow your Vue.js application to retrieve and manipulate data from a server-side database. This means you can fetch data such as product information, user details, or any other relevant data from the server and use it within your Vue.js application. The API provides a consistent interface, enabling your Vue.js application to interact with the server and perform operations on the data seamlessly.

**Language Agnostic**:
APIs are language-agnostic, which means they are not tied to a specific programming language. In this case, your Vue.js application can communicate with the Laravel API regardless of the programming language used to build the API. This flexibility allows you to choose the programming language that best suits your Vue.js application, knowing that it can still interact with the Laravel API.

**Consistent Data Format (JSON)**:
The data exchanged between your Vue.js application and the Laravel API will typically use JSON (JavaScript Object Notation) as the data interchange format. JSON is a lightweight and widely adopted format for structuring and transmitting data. Vue.js, being a JavaScript framework, can easily work with JSON data. JSON provides a simple and standardized way of representing data, making it easy to parse, manipulate, and display within your Vue.js application.

**Separation of Concerns**:
By building a Laravel API, you can separate the data retrieval and manipulation logic from the presentation layer of your Vue.js application. The Laravel API will handle the tasks related to fetching data from the database, performing business logic, and preparing the data for consumption. This separation of concerns makes your application more modular, maintainable, and easier to understand, as each part can focus on its specific responsibilities.

**Scalability and Extensibility**:
As your application grows, the Laravel API allows you to scale and extend your system's functionality without impacting your Vue.js application. You can add new endpoints to the API to support additional features, integrate with third-party services, or handle more complex operations. This scalability and extensibility ensure that your application can evolve and adapt to changing requirements.

**Security and Authentication**:
The Laravel API provides a robust framework for implementing authentication and security measures. You can enforce authentication mechanisms such as token-based authentication, OAuth, or JWT (JSON Web Tokens) to ensure that only authorized users can access certain data or perform specific actions. This helps protect sensitive information, maintain data privacy, and control access to your application's resources.

In summary, building a Laravel API for your Vue.js application allows for seamless data retrieval and manipulation, language agnosticism, consistent data format (JSON), separation of concerns, scalability, extensibility, and security measures. The API acts as an intermediary between your Vue.js application and the server-side database, enabling efficient communication and data exchange. By leveraging the Laravel API, you can create a robust and feature-rich application while keeping your codebase organized, maintainable, and secure.

## Requirments
Before you begin programming your Laravel backend, there are several requirements that need to be set up. Here's a list of the requirements and how to install them using Homebrew:

**Homebrew**:
Homebrew is a package manager for macOS that allows you to easily install and manage software packages. If you don't have Homebrew installed, you can install it by opening Terminal and running the following command:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

**PHP**:
Laravel is built using PHP, so you'll need to install PHP on your system. With Homebrew, you can install PHP by running the following command in Terminal:

```bash
brew install php
```

This will install the latest version of PHP available through Homebrew.

**Composer**:
Composer is a dependency management tool for PHP that is used to manage Laravel and its dependencies. You can install Composer by running the following command in Terminal:

```bash
brew install composer
```

This will install Composer globally on your system, allowing you to use it from anywhere.

**MySQL**:
MySQL is a popular relational database management system that is commonly used with Laravel. To install MySQL using Homebrew, run the following command:

```bash
brew install mysql
```

After installing MySQL, you may need to set up a root password and start the MySQL service. Follow the instructions provided in the Terminal after the installation is complete.

**Laravel Installer**:
The Laravel Installer is a command-line tool that helps in setting up new Laravel projects quickly. You can install it globally using Composer by running the following command:

```bash
composer global require laravel/installer
```

This will make the Laravel Installer available as a global command on your system.

Once you have installed all these requirements, you should have PHP, Composer, MySQL, and the Laravel Installer set up on your system. You are then ready to start programming your Laravel backend.

## Creating The Project
in the terminal, within `documents` run this command: 

```bash
laravel new shoes-api
```

This will create you a new laravel project with all the boilerplate code already written for us!

Now pull `shoes-api` into our code editor and lets begin 🔥

## Create Migration for Products
In Laravel, migrations are used to create and modify database tables. You'll need to create a migration file to define the structure of your "products" table. You can use the make:migration Artisan command to generate the migration file.

```bash
php artisan make:migration create_products_table --create=products
```

This will create our migration file, If we go into that newly created file we should see some boiler plate code has been written by laravel for us. If we replace that boilerplate code with: 

```php
<?php

use Illuminate\Database\Migrations\Migration;
use Illuminate\Database\Schema\Blueprint;
use Illuminate\Support\Facades\Schema;

class CreateProductsTable extends Migration
{
    /**
     * Run the migrations.
     *
     * @return void
     */
    public function up()
    {
        Schema::create('products', function (Blueprint $table) {
            $table->id();
            $table->string('image');
            $table->string('name');
            $table->text('description');
            $table->decimal('price', 8, 2);
            $table->integer('stars_full');
            $table->integer('stars_half');
            $table->integer('stars_empty');
            $table->timestamps();
        });
    }

    /**
     * Reverse the migrations.
     *
     * @return void
     */
    public function down()
    {
        Schema::dropIfExists('products');
    }
}

```

Let's break that down: 


**use Illuminate\Database\Migrations\Migration**; and **use Illuminate\Database\Schema\Blueprint**; are namespace declarations that allow you to use Laravel's migration and schema classes within this file.

**use Illuminate\Support\Facades\Schema**; imports the Schema facade, which provides convenient methods for manipulating database schemas.

**class CreateProductsTable extends Migration** defines a new migration class named CreateProductsTable that extends the Migration base class.

**public function up()** is the method responsible for running the migration. It creates the "products" table.

**Schema::create('products', function (Blueprint $table) {** starts the table creation using the Schema facade's create method. It takes a table name ("products") and a closure function.

**$table->id()**; creates an auto-incrementing primary key column named "id" for the "products" table.

**$table->string('image');** adds a "image" column of type "string" to store the image URL or path for a product.

**$table->string('name');** adds a "name" column of type "string" to store the name of a product.

**$table->text('description');** adds a "description" column of type "text" to store the description of a product.

**$table->decimal('price', 8, 2);** adds a "price" column of type "decimal" to store the price of a product with a maximum of 8 digits, 2 of which are decimals.

**$table->integer('stars_full');**, **$table->integer('stars_half');**, and **$table->integer('stars_empty');** add columns to store the ratings of a product. Each of these columns is of type "integer".

**$table->timestamps();** adds two timestamp columns, "created_at" and "updated_at", which are automatically managed by Laravel to track the creation and modification times of a product.
**}** closes the closure function for creating the "products" table.

**public function down()** is the method responsible for reversing the migration. It drops the "products" table if it exists.

**Schema::dropIfExists('products');** drops the "products" table using the `dropIfExists` method of the Schema facade.

By running the migration, Laravel will create the "products" table with the specified columns in your database.

## Running Our Migration
We can run all migrations by using the command: 

```bash
php artisan migrate
```
If we now refresh our database we should see laravel has added our `Products` table

<img width="1180" alt="Screenshot 2023-07-16 at 12 50 10" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/870fb628-07b2-4525-ba93-4d0d25e12ddc">

Lets manually enter our products into the database
<img width="1196" alt="Screenshot 2023-07-16 at 12 53 15" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/174b5bbe-ea07-49b7-a04a-3f6bfe695f0c">

