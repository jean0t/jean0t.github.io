+++
title = 'How to Work With the Filesystem in Python'
description = 'How to work with file system effectively in python with the pathlib module'
date = 2025-03-29T22:26:13-03:00
draft = false
tags = ['programming',]
+++

Python is one of the coolest programming language out there, capable, beautiful and versatile. We can argue about its speed and its true, it isnt the fastest programming language and if you need something to operate in real time, you wouldn't choose it.  
BUT! It is a great tool to a lot of things, making scripts for automation is one of them, or building your own programs and in a lot of programs and scripts what we will be doing? Exactly, file system manipulations! May it be to create files, to read files if they do exist or to iterate over files in a directory.  

My goal with this article is to make you capable of working with files in an easy way as I do now. I only see tutorials of people using complicated manipulations of strings using the OS modules, but it is so... complex needlessly...

## What we will use

Python offers a great module called `pathlib` that helps us manipulate the file system with ease and sometimes even cross platform manipulations that work in both linux and windows.  
First off, go read the documentation [here](https://docs.python.org/3/library/pathlib.html)  
You will familiarize yourself with the functions and also use it as a wiki later when searching for a function or method.

## What it can do
We will be using the class `Path`, so the basic use for pathlib is simply start by importing it that way:  
`from pathlib import Path`  
***

1. Get the home directory dynamically
```python
from pathlib import Path

home_directory = Path.home()
```  
In this case we didn't instanciate the Path class, but used a static method of it.  

2. Iterate in directories
```python
from pathlib import Path

directory = Path.home() / "Downloads"
for file in directory.iterdir():
	if file.is_file():
		print(file)
```  
This example is silly but really instructive, we are getting the downloads directory from the home in a dynamic way! We can instanciate a path and use this `/ 'directory'` to get the directory we want. After that we iterate over the directory with method `path.iterdir()` that returns a generator with the items in the directory, then we make an if statement that analyses if it is a normal file (not a directory or symlinks or whatever) and prints if it fulfills the requirement.  

3. Read/Write from files
```python
from pathlib import Path
file = Path.home() / "random_file.txt"

file.write_text("I will write this to the file") # it will write the string there

# after writing we can read it easily also
file.read_text() # it will return the contents of the file as a string
```  
See? Really easy to manipulate files, we also have write\_bytes() and read\_bytes() if you are working with bytes.  

4. Creating directories
```python
from pathlib import Path

new_directory_path = Path.home() / "SomeNewDirectory" / "AnotherDirectory"
new_directory_path.mkdir(mode=0o777, parents=True, exist_ok=True)
```  
In this case we declare 2 directories, one inside another and we used it with the method `mkdir()`. Pay attention to the parameters we included. 
`mode=0o777` indicates the mode it will be created, basically the permissions the directory will have, if you are familiar with linux you will understand it, the 0o indicates it is Octal.  
`parents=True` indicates that the parents of the directory you want yo be created will also be created if missing, works the same as `mkdir -p`, otherwise it will throw an error.  
`exist_ok=True` avoids the exception to be raised, because if the directory already exists and exists\_ok is false, then it will stop the execution due to an exception.  

## Conclusion
It is an amazing module, don't you think? Since I discovered it I use everytime I need to make file manipulations and what catches me is how low is the number of people talking about it, at least in the posts about python I see.  
I hope you have enjoyed and learned something new today that you will start applying in your projects or who knows refactoring an old project that used the OS module and is full of complicated string manipulations.
