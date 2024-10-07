# Running a Pre-made Laravel Source Code

Follow these steps to set up and run a pre-made Laravel project:

## Prerequisites

Ensure you have the following installed:

- PHP
- Composer
- Node.js & npm
- MySQL or any other supported database

## Installation Steps

1. **Open terminal**

   ```bash
   open terminal on the source code folder
   ```

2. **Install PHP Dependencies**

   ```bash
   composer install
   ```

3. **Install Node.js Dependencies**

   ```bash
   npm install
   ```

4. **Environment Configuration**

   - If `.env` file is available, skip this step.
   - Otherwise, copy the example environment file:

   ```bash
   cp .env.example .env
   ```

5. **Generate Application Key**

   ```bash
   php artisan key:generate
   ```

6. **Set Up Database**

   - Ensure your MySQL server is running.
   - Create a new database for your project.
   - Update the `.env` file with your database credentials:

   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=your_database_name
   DB_USERNAME=your_database_user
   DB_PASSWORD=your_database_password
   ```

   - Run the migrations:

   ```bash
   php artisan migrate
   ```

7. **Configure Mail Settings**

   - Update the `.env` file with your mail server credentials:

   ```env
   MAIL_MAILER=smtp
   MAIL_HOST=smtp.example.com
   MAIL_PORT=587
   MAIL_USERNAME=your-email@example.com
   MAIL_PASSWORD=your-email-password
   MAIL_ENCRYPTION=tls
   MAIL_FROM_ADDRESS=your-email@example.com
   MAIL_FROM_NAME="${APP_NAME}"
   ```

8. **Run the Development Server**

   ```bash
   php artisan serve
   ```

9. **Compile Assets**
   ```bash
   npm run dev
   ```

Your Laravel application should now be up and running. Access it via `http://localhost:8000`.

## Additional Commands

- **Building Assets for Production**

  ```bash
  npm run build
  ```

- **Clearing Cache (if something isn't working properly)**
  ```bash
  php artisan optimize:clear
  ```
