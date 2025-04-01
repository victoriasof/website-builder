# Website Builder

This is a portfolio website built using **HTML**, **CSS**, **JavaScript**, **PHP**, and **MySQL**. It includes a contact form with database integration, a dark mode toggle, and a responsive design.

---

## Live Demo
You can view the live version of the website here:  
[http://victoriasofianidou.infinityfreeapp.com/?i=1](http://victoriasofianidou.infinityfreeapp.com/?i=1)

---

## Tools and Technologies Used
- **Frontend**: HTML, CSS, JavaScript
- **Backend**: PHP
- **Database**: MySQL
- **Local Server**: XAMPP
- **FTP Client**: FileZilla
- **Hosting**: InfinityFree
- **Database Management**: phpMyAdmin

<<<<<<< HEAD
---

## Features
- **Portfolio Sections**:
  - "Over Mij" (About Me)
  - "Mijn Projecten" (My Projects)
  - "Contacteer Mij" (Contact Me)
- **Dark Mode Toggle**: Allows users to switch between light and dark themes.
- **Contact Form**: Saves user messages to a MySQL database.
- **Responsive Design**: Works on both desktop and mobile devices.

---

## Steps to Create and Deploy the Project

### 1. Create the Website Structure
- Designed the main structure of the website in `index.html`:
  - Header with navigation links.
  - Sections for "About Me," "Projects," and "Contact."
  - Footer with copyright information.

### 2. Style the Website
- Styled the website using `styles.css`:
  - Added styles for layout, typography, and responsiveness.
  - Implemented a **dark mode** feature using the `body.dark-mode` class.

### 3. Add a Contact Form
- Added a contact form in the "Contact" section of `index.html`:
  - Fields for **name**, **email**, and **message**.
  - Form submission handled by `contact.php`.

### 4. Create the PHP Backend
- Created `contact.php` to handle form submissions:
  - Used **MySQLi** to connect to the database.
  - Inserted form data into the `contact_messages` table.
  - Displayed success or error messages after submission.

### 5. Set Up the MySQL Database
- Designed the `contact_messages` table in MySQL:
  ```sql
  CREATE TABLE `contact_messages` (
    `id` int(11) NOT NULL AUTO_INCREMENT,
    `name` varchar(255) NOT NULL,
    `email` varchar(255) NOT NULL,
    `message` text NOT NULL,
    `submitted_at` timestamp NOT NULL DEFAULT current_timestamp(),
    PRIMARY KEY (`id`)
  ) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;
  ```

- Inserted sample data for testing:
  ```sql
  INSERT INTO `contact_messages` (`name`, `email`, `message`, `submitted_at`) VALUES
  ('Victoria', 'victoria.sofianidou@gmail.com', 'Hello!', '2025-03-30 20:17:41');
  ```

### 6. Deploy the Website
- **Local Testing**:
  - Used **XAMPP** to test the website locally.
  - Placed the project files in the `htdocs` directory.
  - Accessed the website at `http://localhost/Website%20builder`.

- **Hosting**:
  - Uploaded the project to **InfinityFree** using **FileZilla**.
  - Imported the database using **phpMyAdmin**.
  - Configured the `config.php` file with the hosting database credentials.

---

## How to Set Up Locally

### 1. Clone the Repository
Clone the repository to your local machine:
```bash
git clone https://github.com/victoriasof/website-builder.git
```

### 2. Set Up a Local Server
Use a local server like **XAMPP** or **WAMP**:
1. Place the project folder in the `htdocs` directory (for XAMPP).
2. Start the Apache and MySQL services.

### 3. Import the Database
1. Open **phpMyAdmin** in your browser:
   ```
   http://localhost/phpmyadmin
   ```
2. Create a new database (e.g., `website_builder`).
3. Import the `website_builder.sql` file into the database.

### 4. Configure the Database
Update the `config.php` file with your database credentials:
```php
<?php
$servername = "your-database-host";
$username = "your-database-username";
$password = "your-database-password";
$dbname = "website_builder";
?>
```

### 5. Access the Website
Open the website in your browser:
```
http://localhost/Website%20builder
```

---

## Future Improvements
- Add email notifications using PHPMailer.
- Enhance the design with animations and transitions.
- Add more projects to the portfolio section.

---

## Author
**Victoria Sofianidou**  
[GitHub Profile](https://github.com/victoriasof)
