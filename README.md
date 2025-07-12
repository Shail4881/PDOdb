# PDOdb: A Simple PDO-based Database Class for PHP Applications

![PDOdb](https://img.shields.io/badge/PDOdb-Database%20Class-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
![License](https://img.shields.io/badge/license-MIT-lightgrey.svg)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [Topics](#topics)
- [Contributing](#contributing)
- [License](#license)
- [Releases](#releases)

## Overview

PDOdb is a PHP database class designed to work seamlessly with ThingEngineer-compatible databases. It provides a simple and efficient way to interact with your database using PDO (PHP Data Objects). This class acts as a wrapper around PDO, making database interactions straightforward and secure.

## Features

- **Database Abstraction Layer**: Simplifies database interactions.
- **Supports MySQLi and PDO**: Flexibility to choose your database driver.
- **Query Builder**: Build complex SQL queries easily.
- **Security**: Prevents SQL injection and other vulnerabilities.
- **PHP 8 Compatibility**: Fully supports the latest PHP features.
- **Easy Integration**: Works well with existing PHP applications.

## Installation

To install PDOdb, clone the repository or download it as a ZIP file. 

```bash
git clone https://github.com/Shail4881/PDOdb.git
```

Alternatively, you can download the ZIP file from the [Releases](https://github.com/Shail4881/PDOdb/releases) section.

## Usage

Using PDOdb is straightforward. Here’s a simple example to get you started:

```php
require 'PDOdb.php';

$db = new PDOdb('mysql:host=localhost;dbname=testdb', 'username', 'password');

// Create a new table
$db->query("CREATE TABLE users (id INT PRIMARY KEY AUTO_INCREMENT, name VARCHAR(100))");

// Insert data
$db->insert('users', ['name' => 'John Doe']);

// Fetch data
$users = $db->select('users');
print_r($users);
```

## Examples

### Connecting to the Database

To connect to your database, use the following code:

```php
$db = new PDOdb('mysql:host=localhost;dbname=testdb', 'username', 'password');
```

### Executing Queries

You can execute any SQL query directly:

```php
$db->query("SELECT * FROM users");
```

### Inserting Data

Inserting data is simple with the insert method:

```php
$db->insert('users', ['name' => 'Jane Doe']);
```

### Fetching Data

To fetch data from the database:

```php
$users = $db->select('users');
```

### Updating Data

You can also update existing records:

```php
$db->update('users', ['name' => 'John Smith'], ['id' => 1]);
```

### Deleting Data

Deleting records is just as easy:

```php
$db->delete('users', ['id' => 1]);
```

## Topics

- **Database Abstraction Layer**: Provides a unified interface for different database systems.
- **MySQLi and PDO**: Supports both MySQLi and PDO, giving developers flexibility.
- **PDO-MySQL**: Utilizes the PDO extension for MySQL, ensuring secure database interactions.
- **PDO Wrapper**: Simplifies database operations with a user-friendly interface.
- **PHP 8**: Fully compatible with PHP 8 features, ensuring modern development practices.
- **Query Builder**: Helps construct SQL queries programmatically.
- **Replacement**: Acts as a replacement for traditional database classes.
- **Security**: Built-in protections against common security threats.

## Contributing

Contributions are welcome! If you have suggestions or improvements, feel free to open an issue or submit a pull request. Please ensure your code adheres to the existing style and includes tests where applicable.

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Releases

For the latest releases, visit the [Releases section](https://github.com/Shail4881/PDOdb/releases). Download the latest version and execute it in your project.

---

Feel free to explore the features and capabilities of PDOdb. This class aims to simplify your database interactions while maintaining security and efficiency. Whether you're building a new application or integrating into an existing one, PDOdb offers the tools you need to succeed.