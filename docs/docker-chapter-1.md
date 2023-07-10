# Tutorial: Creating a Docker Clone in Bash

## Introduction

In this tutorial, we will learn how to create a simplified clone of Docker using the Bash scripting language. Docker is a popular tool used for containerization, allowing developers to package applications and their dependencies into isolated, lightweight containers.

Throughout this tutorial, we will gradually build a basic Docker clone called "mocker." mocker will provide a subset of Docker's functionality, allowing us to create and manage containers, pull images from a registry, execute commands within containers, and more.

By the end of this tutorial, you will have a solid understanding of containerization concepts, Unix command-line tools, and Bash scripting. Let's get started!

## Chapter 1: Setting Up the Project

### Prerequisites

Before we begin, make sure you have the following prerequisites installed on your system:

- A Unix-like operating system (e.g., Linux or macOS)
- Bash (version 4 or later)
- Basic knowledge of the Unix command line

### Project Structure

To organize our project, we'll create a directory called "mocker" to hold our scripts and files. Open a terminal and run the following command to create the directory:

```bash
mkdir mocker
```

Change to the project directory using the following command:

```bash
cd mocker
```

### Script Initialization

Inside the "mocker" directory, create a new file called "mocker.sh" using your preferred text editor. This file will serve as our main script for the mocker tool.

```bash
touch mocker.sh
```

Open "mocker.sh" in your text editor and add the following shebang line at the top of the file. This line tells the system to execute the script using the Bash interpreter.

```bash
#!/usr/bin/env bash
```

Save the changes and make the script executable using the following command:

```bash
chmod +x mocker.sh
```

Now we have our initial setup ready. In the next chapter, we'll start implementing the functionality to create an image from a directory.