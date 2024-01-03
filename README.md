# Python3
python notes
# https://learn.microsoft.com/en-us/training/modules/python-create-manage-projects/2-set-up-project
What's a virtual environment?
You have a development machine. On that machine, you might have one version of Python installed or one version of a library that you meant to use. What happens when you move your program to a machine that has a different version of Python installed or different versions of the libraries that you depend on?

One thing you don't want to do is assume that your program will work and that you can just install the latest version of whatever libraries you depend on. If you do that, you might end up destroying the ability of the other programs to function on the target machine. The solution is to find a way for your app to work in isolation.

Python's solution for these problems is a virtual environment. A virtual environment is a self-contained copy of everything needed to run your program. This includes the Python interpreter and any libraries your program needs. By using a virtual environment, you can ensure your program will have access to the correct versions and resources to run correctly.

The basic workflow looks like this:

Create a virtual environment that won't affect the rest of the machine.
Step into the virtual environment, where you specify the Python version and libraries that you need.
Develop your program.
Create a virtual environment
You create a virtual environment by calling the venv module. The module expects a name as an argument. You'll set up your own virtual environment in the next unit, so you don't need to run any of the following code.

Take the following steps:

Go to the directory where you want to keep your project.

Use the following command to call the venv module.

Console

Copy
python -m venv env
At this point, some directories are created for you. The directory names differ slightly depending on your operating system.

The directories look like this in Windows:

Output

Copy
/env
  /include
  /lib
  /Scripts
The directories look like this in Linux and macOS:

Output

Copy
/env
  /bin
  /include
  /lib
Your environment needs the env directory to keep track of details like which version of Python and which libraries you're using. Don't put your program files in the env directory. We suggest that you put your files in a directory called src or something similar. The project structure might then look like this:

Output

Copy
/env
/src
  program.py  
Activate the virtual environment
At this point, you have a virtual environment, but you haven't started using it. To use it, you need to activate it by calling an activate script.

Here's how the activation looks on Windows:

Console

Copy
C:\ .. \env\Scripts\activate
Here's how the activation looks on Linux and macOS:

Bash

Copy
source env/bin/activate
Calling activate changes your prompt. It's now preceded with (env) and looks something like this example:

Output

Copy
(env) -> path/to/project
At this point, you're inside your virtual environment. Anything you do happens in isolation
