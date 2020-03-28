# Installing & Running the System

It is super simple to run LaraEstimate. First, you need to check if all the [requirements](REQUIREMENTS.md) are installed on your system. After it, follow these steps:

## 1. Create a new Database
Create a new MySQL Database. We recommend that you use utf8mb4 charset in your database ([See why here](https://stackoverflow.com/questions/766809/whats-the-difference-between-utf8-general-ci-and-utf8-unicode-ci)). You can create it using the following command, or using your preferred database manager:

```CREATE DATABASE laraestimate CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;```

## 2. Extract the Code
Extract the code in a directory of your preference. Then, navigate to the project folder using the terminal and install all the composer packages with the command below:

```
composer install
```

The composer packages installation can take a few minutes. After the installation, inside the project folder, find a file called:

```
.env.example
```

Copy all the .env.example file content to a new file called:

```
.env
```

Inside this new **.env** file, change the DATABASE section to use the database you have created in the first step:

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=laraestimate
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

## 3. Create the Symbolic Link for files storage

LaraEstimate uses the awesome package [Laravel MediaLibrary](https://github.com/spatie/laravel-medialibrary) with the Public Disk configuration to save the uploaded files.

To configure the Public Disk, access your LaraEstimate project folder from the terminal and run this command:

```
php artisan storage:link
```

After it, your LaraEstimate installation can make file and image uploads.

## 4. Creating the database tables and seeding the data

Now, inside your LaraEstimate project folder, you can run the commands to create the database tables and seed the test data. If you want to seed the system with all the *fake test data*, run the command below:

```
php artisan migrate --seed
```

Or, if you want a clean database, use this command:

```
php artisan migrate
```

And then, run the following command to create an **Admin user (email: admin@admin.com, password: password)** on your system:

```
php artisan db:seed --class=AdminUserTableSeeder
```

## 5. Running the System
Inside your LaraEstimate project folder, execute this command to generete de **APP_KEY**:

```
php artisan key:generate
```

And this command to run a server in the http://localhost on the port 8000:

```
php artisan serve
```

And then, access [http://localhost:8000](http://localhost:8000) to see LaraEstimate running.

## 6. Default Logins
After seeding the system data, it will create this default login:

Admin - email: admin@admin.com, password: password

That's all, do the login and enjoy creating Estimates!