## Chapter 2: Implementing a Docker Clone - Overview and Subvolumes

In this chapter, we'll provide an overview of our Docker clone, named "mocker," and discuss the key components involved. We'll also explain the concept of subvolumes and their role in creating and managing container images.

### Overview of the Docker Clone

Our Docker clone, "mocker," aims to replicate some of the core functionalities of Docker using Bash scripting. While not as feature-rich or extensive as Docker itself, mocker will provide a simplified version of containerization for users to create and manage containers.

To achieve this, we'll utilize various Linux command-line tools and concepts, including subvolumes, namespaces, and cgroups. We'll implement functions that emulate Docker's image and container management functionalities, such as image creation, image pulling, container creation, container management, and more.

### Key Components

Let's briefly discuss the key components of our Docker clone:

1. **Subvolumes**: In our implementation, we'll utilize Btrfs subvolumes as a lightweight and efficient way to manage container images and container file systems. A subvolume is a standalone, independent snapshot of a file system within a Btrfs file system. We can treat subvolumes as the building blocks for our container images and containers.

   By utilizing subvolumes, we can create isolated file systems for each container, providing encapsulation and separation from the host system. This isolation enables containers to have their own file system, libraries, binaries, and configurations without interfering with other containers or the host system.

   We'll use subvolumes to create and manage container images, which serve as the blueprint for launching containers.

2. **Namespaces**: Linux namespaces are a crucial feature that enables process isolation within our containers. Namespaces allow us to create separate instances of various system resources, such as process IDs, network interfaces, mount points, and more. This isolation ensures that processes within a container remain isolated and do not interfere with processes outside the container or other containers.

   We'll utilize namespaces to isolate the process IDs, network interfaces, mount points, and other system resources of our containers, providing a level of isolation and ensuring that containers operate independently.

3. **Cgroups**: Control Groups (cgroups) allow us to manage and limit the resource usage of containers. With cgroups, we can control and allocate system resources such as CPU, memory, disk I/O, and network bandwidth to ensure fair sharing and prevent any single container from monopolizing resources.

   By utilizing cgroups, we can impose resource restrictions and limits on our containers, enabling fine-grained control over resource allocation and preventing any single container from adversely affecting others or the overall system performance.

These components, combined with various Linux command-line tools and utilities, will form the foundation of our Docker clone implementation.

In the next chapter, we'll dive into the implementation details of the `mocker_init` function, which enables the creation of container images from directories using Btrfs subvolumes.

That concludes Chapter 2. In the next chapter, we'll implement the `mocker_init` function.
