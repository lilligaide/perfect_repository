# learn2code

This repository contains slides, exercise examples and more for my lecture "Software Development".

All documents are located in the folder [docs](docs). The documents are completely written in markdown and are optimized for [marp](https://marp.app/).

- [Content of the Lecture](#content-of-the-lecture)
- [Prepared Environments](#prepared-environments)
- [How to Create the Slides](#how-to-create-the-slides)
- [How to Build the Code](#how-to-build-the-code)

## Content of the Lecture

### Part I
In the first part of the lecture, the programming language **C** is introduced.
On the one hand, the lecture deals with the necessary basics like *datatypes, structures, arrays, pointers, branching, looping*, and many more. On the other hand, basic tools of software engineering are introduced. Among others, these tools are: *Linux Terminal, GCC, Clang, Git, CMake, google-test, VS Code, clang-format*, and some more. 

The slides of the first part of the lecture can be found in [slides_learn2code_1.md](docs/slides_learn2code_1.md). Respectively, the content of the first part is given in the [Table of Contents](docs/slides_learn2code_1.md#table-of-contents).

For each part of the lecture, the corresponding [code](code) can be found.
Further, there are some homeworks. The homeworks for part I are named *Homework_1-\*.md* and can be found in de folder [docs](docs). The solutions to the homeworks are again to be found in the [code](code) folder.

### Part II
In the second part of the lecture, the programming language **C++** is introduced.
This part is currently under construction. Expected content could be (incomplete):
- doxygen
- clang-tidy
- from C to C++
- dynamic memory in C, C++, and C++14 (and later)
- namespaces
- stl and some basic containers (like string, vector, array, queues, ...)
- inheritance
- polymorphism
- open topics
  - static_asserts??
  - opencv examples??
  - Qt examples??

## Prepared Environments 

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=545666306&machine=basicLinux32gb&location=WestEurope)

<a href="https://gitpod.io/#git@github.com:BenniWi/learn2code.git">
  <img
    src="https://img.shields.io/badge/Contribute%20with-Gitpod-908a85?logo=gitpod"
    alt="Contribute with Gitpod"
  />
</a>

## How to Create the Slides

### Install Latest nodejs
https://tecadmin.net/install-latest-nodejs-npm-on-ubuntu/
```sh
sudo apt install -y curl 
curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash - 
```

### Install Marp
```sh
npm install -g @marp-team/marp-cli
```

### Install google-chrome
```sh
wget -q https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
sudo apt-get install ./google-chrome-stable_current_amd64.deb
rm ./google-chrome-stable_current_amd64.deb
```

### Possible Marp Call
```sh
marp -c docs/marp_config.yaml docs/slides_learn2code_1.md
```

## How to Build the Code
Most of the code samples are supporting [CMake](https://cmake.org/).
All *CMake* capable samples are collected in the top-level [CMakeLists.txt](CMakeLists.txt).
Configure this top level project and your good to go.

For all non CMake samples you should use the compiler of your joice (mostly [gcc](https://gcc.gnu.org/) or [clang](https://clang.llvm.org/) and build it manually.
