# website-builder

http://victoriasofianidou.infinityfreeapp.com/?i=1

html, css, javascript, php 

XAMPP 

FileZilla Client 

InfinityFree

phpMyAdmin

MySQL Database 

CREATE TABLE `contact_messages` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `name` varchar(255) NOT NULL,
  `email` varchar(255) NOT NULL,
  `message` text NOT NULL,
  `submitted_at` timestamp NOT NULL DEFAULT current_timestamp(),
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;
