# Laravel API
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

## Create Model for Products
In Laravel, models represent database tables and handle interactions with the database. Create a model for your "products" table using the make:model Artisan command. In the console type:

```bash
php artisan make:model Product
```

This will create a "Product" model file in the `app/Models` directory. Again there will be some boilder plate here but we can replace it with this: 

```php
<?php

namespace App\Models;

use Illuminate\Database\Eloquent\Factories\HasFactory;
use Illuminate\Database\Eloquent\Model;

class Product extends Model
{
    use HasFactory;

    /**
     * The table associated with the model.
     *
     * @var string
     */
    protected $table = 'products';

    /**
     * The attributes that are mass assignable.
     *
     * @var array
     */
    protected $fillable = [
        'image',
        'name',
        'description',
        'price',
        'stars_full',
        'stars_half',
        'stars_empty',
    ];

    /**
     * The attributes that should be hidden for arrays.
     *
     * @var array
     */
    protected $hidden = [];

    /**
     * The attributes that should be cast to native types.
     *
     * @var array
     */
    protected $casts = [
        'id' => 'integer',
        'price' => 'decimal:2',
        'stars_full' => 'integer',
        'stars_half' => 'integer',
        'stars_empty' => 'integer',
    ];
}
```

Let's break down the different sections of the "Product" model:

**Namespace and Use Statements**:
The model file resides in the App\Models namespace, so the namespace declaration reflects that. The use statements import the necessary classes for the model.

**Class Definition**:
The Product class extends the base Model class provided by Laravel. It also uses the HasFactory trait, which enables model factories to create fake instances for testing purposes.

**Table Name**:
The $table property specifies the name of the database table associated with the model. In this case, it is set to 'products', which matches the name of your "products" table.

**Mass Assignable Attributes**:
The $fillable property defines an array of attributes that can be mass-assigned when creating or updating a product. In this example, it includes attributes such as 'image', 'name', 'description', 'price', 'stars_full', 'stars_half', and 'stars_empty'.

**Hidden Attributes**:
The $hidden property is an array of attributes that should be hidden when the model is converted to an array or JSON response. By default, it is empty, but you can specify any attributes you want to hide from public view.

**Attribute Casting**:
The $casts property defines how certain attributes should be cast to specific data types. In this example, the 'id' attribute is cast as an integer, 'price' as a decimal with two decimal places, and 'stars_full', 'stars_half', and 'stars_empty' as integers.

These sections help configure the model's behavior when interacting with the database and defining the attributes that can be assigned, hidden, or casted.

## Create Controller for Products:
Controllers handle the logic and operations related to your API endpoints. Create a controller for handling products using the make:controller Artisan command. In the terminal type:

```bash
php artisan make:controller ProductController --api
```

This will create a "ProductController" file in the app/Http/Controllers directory. In the controller, you'll define methods to handle different API actions, such as fetching all products, creating a product, updating a product, etc. If we go to the file, you will again see placeholder content that laravel has provider. We can remove this and instead enter: 

```php
<?php

namespace App\Http\Controllers;

use App\Models\Product;
use Illuminate\Http\Request;
use Illuminate\Http\Response;

class ProductController extends Controller
{
    /**
     * Display a listing of the products.
     *
     * @param  \Illuminate\Http\Request  $request
     * @return \Illuminate\Http\Response
     */
    public function index(Request $request)
    {
        $products = Product::all();

        return response()->json([
            'data' => $products,
        ]);
    }

    /**
     * Display the specified product.
     *
     * @param  \Illuminate\Http\Request  $request
     * @param  \App\Models\Product  $product
     * @return \Illuminate\Http\Response
     */
    public function show(Request $request, Product $product)
    {
        return response()->json([
            'data' => $product,
        ]);
    }

    /**
     * Store a newly created product in storage.
     *
     * @param  \Illuminate\Http\Request  $request
     * @return \Illuminate\Http\Response
     */
    public function store(Request $request)
    {
        $validatedData = $request->validate([
            'image' => 'required|string',
            'name' => 'required|string',
            'description' => 'required|string',
            'price' => 'required|numeric',
            'stars_full' => 'required|integer',
            'stars_half' => 'required|integer',
            'stars_empty' => 'required|integer',
        ]);

        $product = Product::create($validatedData);

        return response()->json([
            'data' => $product,
        ], Response::HTTP_CREATED);
    }
}
```

Now let's break down the different sections of the "ProductController":

**Namespace and Use Statements**:
The controller file resides in the App\Http\Controllers namespace. The use statements import the necessary classes, including the Product model and other dependencies.

**Class Definition**:
The ProductController class extends the base Controller class provided by Laravel.

**Index Method**:
The index method handles the request to fetch all products. It retrieves all products using the Product::all() method and returns a JSON response with the products' data.

**Show Method**:
The show method handles the request to fetch a specific product. It accepts a Product model instance through route model binding, where the product ID is automatically resolved from the request URL. It returns a JSON response with the specific product's data.

**Store Method**:
The store method handles the request to create a new product. It starts by validating the incoming request data using the validate method, which ensures that the required fields (image, name, description, price, stars_full, stars_half, and stars_empty) are present and have the specified validation rules. If the validation passes, a new Product instance is created using the create method, which assigns the validated data to the corresponding attributes. Finally, a JSON response is returned with the created product's data, along with the HTTP_CREATED status code.

These are just a few example methods, but you can add additional methods to the controller as needed, such as methods for updating, deleting, or performing other actions on products.

In your controller, you'll define the necessary methods to handle different API actions based on your requirements. Each method receives an instance of the Request object, allowing you to access the incoming request data, query parameters, and more. You'll also utilize the Response object to generate appropriate JSON responses with the desired HTTP status codes.

## Define API Routes
In Laravel, routes define the endpoints and map them to the corresponding controller methods. Open the routes/api.php file.

The api.php file is one of the route files in Laravel and specifically designed for defining API routes. Routing is the process of determining how an application responds to a client request. In Laravel, routes serve as the entry points for different HTTP requests and map them to specific controller methods. By defining routes, you can specify which URLs should trigger which actions in your application.

We can replace the boilerplate in api.php with: 

```php
<?php

use Illuminate\Http\Request;
use Illuminate\Support\Facades\Route;
use App\Http\Controllers\ProductController;

Route::get('/products', [ProductController::class, 'index']);
Route::get('/products/{product}', [ProductController::class, 'show']);
Route::post('/products', [ProductController::class, 'store']);
```

Let's explain the different sections of the api.php file:

**Namespace and Use Statements**:
The file starts with use statements to import necessary classes, such as Route and the ProductController.

**Route Definitions**:
The Route facade is used to define the routes. In this example, three routes are defined:
Route::get('/products', [ProductController::class, 'index']); maps the GET /products URL to the index method in the ProductController.

**Route::get('/products/{product}', [ProductController::class, 'show'])**; maps the GET /products/{product} URL to the show method in the ProductController. The {product} parameter is a route parameter and allows you to retrieve a specific product based on its ID or unique identifier.

**Route::post('/products', [ProductController::class, 'store'])**; maps the POST /products URL to the store method in the ProductController. This route is used for creating a new product.

**Request and Response Objects**:
The Request object is automatically available within the route closures or controller methods. It represents the incoming HTTP request and provides access to request parameters, headers, and more.

**Controller Method References**:
The controller methods are referenced using an array syntax: [ProductController::class, 'method']. The first element is the fully qualified class name of the controller, and the second element is the method name that should be invoked when the route is accessed.

By defining these routes, you're specifying the URL endpoints that correspond to specific actions in your API. When a client makes a request to one of these endpoints, Laravel will route the request to the appropriate controller method, which will handle the logic and generate the response.

So what happens when a User in their web browser goes to `/api/products`: 

`/api/products` goes through the defined route, controller, model, and eventually reaches the index method:

**User Request**:
When a user makes a request to the /api/products URL, their request is sent to the server.

**Routing**:
Laravel's routing system receives the user request and matches it against the defined routes in the api.php file. In this case, the request matches the Route::get('/products', [ProductController::class, 'index']) route definition.

**Controller Resolution**:
Once the routing system identifies the matching route, it knows that the request should be handled by the ProductController. Laravel resolves the controller class and prepares to execute the corresponding method.

**Controller Method Execution**:
The routing system identifies that the index method in the ProductController should handle the request. It calls the index method and passes any necessary arguments (such as the Request object).

**Controller Logic**:
Inside the index method of the ProductController, you can write the necessary logic to handle the request. In this case, the logic might involve retrieving all products from the database using the Product::all() method.

**Model Interaction**:
The ProductController interacts with the Product model to fetch the data. In the index method, you might call the all() method on the Product model, which retrieves all products from the database.

**Response Generation**:
After retrieving the data from the model, the controller prepares a response. In this case, it might use Laravel's response() helper method to create a JSON response. The data retrieved from the model is included in the response.

**Response Sent to User**:
Finally, the controller sends the response back to the user who made the initial request. The user receives the JSON response containing the product data.

This process ensures that when a user visits /api/products, the request is correctly routed to the ProductController and its index method. The controller then interacts with the model to fetch the necessary data and generates a response that is sent back to the user.

Let's now see the result in the browser! In the terminal type: 

```bash
php artisan serve
```
This will start a local server where our api can be accessed from. You should see something like `   INFO  Server running on [http://127.0.0.1:8000].  ` 

going to that url you will see the applicaiton, if you add `/api/proucts` you should see: 

<img width="1015" alt="Screenshot 2023-07-16 at 13 19 09" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/1cf34983-0cf1-4090-8460-768187e3ac8b">

## Updating our Vue.js Application To Retrieve Products From Our API
Keeping our API running in the background, if we load up our `shoes-frontend` project and go into the `NewArival.vue` component. You will see currently that it's getting the Products from a static array of objects we manually defined:

```vue
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
```

But now that we have a API that GETS the products from a database we should modify this!

Modify NewArrival.vue to be: 

```vue
<template>
  <div class="products" id="Products">
    <h1>Products</h1>
    <div class="box">
      <ProductCard v-for="product in products" :key="product.id" :product="product" />
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
      products: []
    }
  },
  mounted() {
    this.fetchProducts();
  },
  methods: {
    fetchProducts() {
      fetch('http://127.0.0.1:8000/api/products')
        .then(response => response.json())
        .then(data => {
          this.products = data.data;
        })
        .catch(error => {
          console.error('Error fetching products:', error);
        });
    }
  }
}
</script>

<style scoped>
.products {
  width: 100%;
  height: 140vh;
  padding: 25px 0;
}

.products h1 {
  margin: 35px 0;
  font-size: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  text-transform: uppercase;
  background: linear-gradient(to right, #c72092, #6c14d0);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.products .box {
  width: 90%;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-gap: 25px 0;
}
</style>
```

Modify ProductCard.vue to be: 

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
        <i class="fa-solid fa-star" v-for="i in parseInt(product.stars_full)" :key="i"></i>
        <i class="fa-solid fa-star-half-stroke" v-if="product.stars_half"></i>
        <i class="fa-regular fa-star" v-for="i in parseInt(product.stars_empty)" :key="i"></i>
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
  background: linear-gradient(to right, #c72092, #6c14d0);
  color: white;
}
</style>
```

Let's explain the lifecycle hooks and the Fetch API, and how we utilize them in this scenario:

**Lifecycle Hooks, specifically the mounted hook**:
Lifecycle hooks are methods provided by Vue.js that allow you to perform certain actions at different stages of a component's lifecycle. The mounted hook is one of the lifecycle hooks, and it is called after the component has been mounted onto the DOM. This hook is commonly used to perform initial setup, fetch data from APIs, or interact with external libraries.

In the given code, the mounted hook is used to call the fetchProducts method. This ensures that when the component is mounted onto the DOM, the fetchProducts method is automatically invoked, fetching the products data from the API.

**The Fetch API**:
The Fetch API is a modern web API that provides a built-in mechanism for making HTTP requests in JavaScript. It offers a simple and powerful way to handle network requests and responses.

In the fetchProducts method, we use the Fetch API to make a GET request to the specified URL (http://127.0.0.1:8000/api/products). The fetch function initiates the request and returns a Promise that represents the eventual response. We can then chain .then() methods to handle the response asynchronously.

**Handling the Response**:
Inside the .then() method, we call response.json() to parse the response body as JSON. This returns another Promise that resolves to the JSON data contained in the response. We then chain another .then() method to access the parsed JSON data.

**Updating the Component State**:
Finally, inside the second .then() method, we assign the fetched data to the products array using this.products = data.data. Assuming the API response includes an object with a data property containing the array of products, we extract that array and update the products data property of the Vue component. This will trigger a re-rendering of the component, displaying the fetched products on the page.

**Error Handling**:
In case of an error during the fetch request, the .catch() method is called. It logs the error to the console using console.error() to help with debugging and error tracking.

By utilizing the mounted lifecycle hook and the Fetch API, we ensure that the fetchProducts method is called when the component is mounted, making a request to the specified API endpoint and updating the products data property with the fetched data. This allows the Vue component to display the products on the page after they have been fetched from the API.

In our database, lets make it realy obvious that our data is coming from the API, modify one of the database entries like so
<img width="945" alt="Screenshot 2023-07-16 at 13 41 56" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/763a0c7d-5b3b-450c-a781-c5d4189b89fb">

if we look at this in the browser we should see:

<img width="1425" alt="Screenshot 2023-07-16 at 13 42 55" src="https://github.com/michaelbarley/new-starter-demo-project/assets/50404794/f4446d08-5ff0-48b4-a3ab-6b710588727d">

# Congratulations

Well done! you made it through this section. We now have our Vue.js application communicating with our very own API. The data is persistant and we can easily add and remove products!





