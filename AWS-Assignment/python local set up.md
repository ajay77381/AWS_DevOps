# How to Install and Run Multiple Python Versions on Ubuntu/Debian 


URL- https://k0nze.dev/posts/install-pyenv-venv-vscode/


To install pyenv on Debian or Ubuntu-based Linux distributions, you have to install several libraries and packages necessary for building Python from scratch. Enter the following command into your terminal to install all necessary packages:

```
sudo apt install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl \
git
```
## To install pyenv you can clone it directly from the [GitHub](https://github.com/pyenv/pyenv) repository:
   
```
1|   git clone https://github.com/pyenv/pyenv.git ~/.pyenv
```

After cloning it you need to enter the following commands to add pyenv to your $PATH and start it when a new terminal is opened (if you use a different shell than bash you have to change ~/.bashrc accordingly):

```
 1|   echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
 2|    echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
 3|     echo 'eval "$(pyenv init --path)"' >> ~/.bashrc

```

###Using  **pyenv** Commond you can check payenv is installed.

After you successfully installed pyenv it is time to look at the different commands that pyenv offers to manage different Python versions.

Probably the most important command is:
```
1 |  pyenv install [PYTHON_VERSION]
```


![Image](https://github.com/users/agileguru/projects/24/assets/130822600/9534243a-8b12-4792-a289-a1ebde1a56c8)



With this command, you can install a specific Python version on your system. To see all versions that are available to install enter:

```
pyenv install -l
```

This will print out a very long list on your terminal (depending on your operating system) of Python versions you can install. And it is not just the standard CPython versions. There is also [pypy](https://en.wikipedia.org/wiki/PyPy), which is an implementation of Python in Python itself. Or anaconda, which is very popular in the sciences and data mining. Pick your preferred Python version and use pyenv install to install it on your system.

To see which versions you already installed on, enter the following command into your terminal:

```
pyenv versions
```

This command will list all the Python versions that you can choose from pyenv. The version that is currently active has an asterisk (*) in front of it:

```
  system
  3.10.0rc1
* 3.9.6 (set by /home/konze/Programming/ml_acc_timing_model_extraction/.python-version)
  pypy3.7-7.3.5
```

#### If you want to know which Python version is currently active in your shell, just type:
```
1| pyenv version
```
Now, after you installed several different versions, how do you set a specific version? To select a default Python version that is active when you open a new terminal, you use the global command:

```
pyenv global [PYTHON_VERSION]

```

Ensure to enter the exact name of the installed Python version shown when you enter pyenv versions. Alternatively to pyenv global [PYTHON_VERSION], you can also set an environment variable (Unix only) PYENV_VERSION with:
```
export PYENV_VERSION=[PYENV_VERSION]

```

If you want to set a specific Python version for your current terminal session, use:
```
pyenv shell [PYTHON_VERSION]

```

This will set the Python version only as long as your session is active. So after you close your terminal, everything is back to default.

To set a project Python version that is active as soon as you “cd” into the project directory, enter the following when you are inside of the project’s root directory:
```
pyenv local [PYTHON_VERSION]

```

This will create the file .python-version that contains the [PYTHON_VERSION]. You can even check that by entering pyenv versions, and it will tell you based on what setting the currently active Python version was selected.

Of course, there are more pyenv commands, but I won’t go into those in this article. You can find a complete command reference over here: [pyenv Command Reference](https://github.com/pyenv/pyenv/blob/master/COMMANDS.md).

### Creating Virtual Environments

The real power of Python comes from its vast amount of modules ranging from graph theory to machine learning. To install those modules, the pip command is used. If you are using pyenv and you enter pip:
```
1|   which pip

```

and for Windows PowerShell:
```
get-command pip
```

It will show you that pip is called from the .pyenv directory. And if you install a module using pip it is installed into your .pyenv directory tied to the currently active version. So if you install numpy while your current Python version is 3.9.6 numpy won’t be available when you switch to anaconda3-2021.05. However, this granularity might not be enough, and you need a project-based distinction between different modules. And virtual environments do exactly that for you.

To create a new virtual environment for your project, open a terminal in your project’s root directory. Make sure you set your desired Python version for this project using pyenv local [PYTHON_VERSION] then enter:
```
1|   python -m venv .venv
```

This command will create a new directory .venv which includes the Python interpreter (provided by pyenv) and all the modules installed using pip later on. After creating the newly created virtual environment, you have to activate it. This is done by entering:
```
source .venv/bin/activate
```












