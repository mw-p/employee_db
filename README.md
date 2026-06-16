# Employee DB

![C](https://img.shields.io/badge/C-95.4%25-blue?style=for-the-badge\&logo=c)
![Makefile](https://img.shields.io/badge/Makefile-4.6%25-orange?style=for-the-badge)
![Project](https://img.shields.io/badge/LowLevelAcademy-learning_project-green?style=for-the-badge)

## 📌 About

**Employee DB** is a small low-level learning project written in **C**.
The application stores employee records in a custom binary database file and allows creating a new database file or appending employee data from the command line.

This project was built as part of learning low-level programming concepts from **LowLevelAcademy**.

## ✨ Features

* Create a new binary database file
* Open and validate an existing database file
* Store employee records with:

  * name
  * address
  * worked hours
* Write and read structured binary data
* Use custom database headers
* Practice low-level C concepts:

  * file descriptors
  * binary file I/O
  * structs
  * memory allocation
  * endianness conversion
  * command-line argument parsing

## 🗂️ Project Structure

```text
employee_db/
├── db/              # Database files
├── include/         # Header files
│   ├── common.h
│   ├── file.h
│   └── parse.h
├── src/             # Source files
│   ├── file.c
│   ├── main.c
│   └── parse.c
├── Makefile
└── README.md
```

## 🛠️ Technologies

* C
* Make
* Linux/POSIX file operations

## 🚀 Getting Started

### Prerequisites

Make sure you have a C compiler and `make` installed.

```bash
gcc --version
make --version
```

### Build

```bash
make
```

This will compile the project and create the final executable in:

```text
bin/final
```

### Clean build files

```bash
make clean
```

## ▶️ Usage

```bash
./bin/final -f <database_file> [options]
```

### Options

| Option | Description                |
| ------ | -------------------------- |
| `-f`   | Path to the database file  |
| `-n`   | Create a new database file |
| `-a`   | Add a new employee record  |

## 📚 Examples

### Create a new database

```bash
./bin/final -n -f ./db/employees.db
```

### Add an employee

```bash
./bin/final -f ./db/employees.db -a "John Doe,123 Main Street,40"
```

The `-a` argument uses the following format:

```text
"name,address,hours"
```

### Run default Makefile example

```bash
make run
```

## 🙌 Credits

Project inspired by **LowLevelAcademy**.
