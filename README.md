# Introduction to Data Science with Python
In this [Houston Data Science][1] meetup we will introduce our members to data science using the Python programming language.

## Objectives

* Install Python 3 and set up on your computer via the Anaconda distribution
* Install Git locally and create a Github account
* Develop Python programs in a text editor, IDE and Jupyter Notebook
* Use the command line to execute a program and run Python interactively
* Use Jupyter Notebook to explore the most popular data science libraries
* Have a huge list of resources to help you continue your data science journey

## Agenda
* Create a Github Account
* Install Git locally
* Fork and clone this respository
* Install Python 3 with Anaconda
* Run Python interactively
* Install Sublime Text 3 along with packages for enhancing development
* Install PyCharm EDU
* Execute basic programs from command line
* PyData
* NumPy
* pandas
* statsmodels
* matplotlib
* seaborn
* connect to sqlite

## Create Github Account
The page is currently being hosted on Github, a site that hosts remote Git repositories. Github is a popular place to share and collaborate on software projects. The most popular data science libraries are all hosted on Github. On Github, you can find the latest developments, track bugs and join the conversation with fellow developers.  

> 1. If you have not already done so, create a Github account now.

## Install Git Locally
Git is a popular version control system used to keep track of file changes during software development. Github is a private company independent from Git. Git is free software that tracks your file changes on your local machine.

Let's install Git on your local machine
> 1. Visit the [Git downloads page][3] and download Git for your operating system.
> 2. After installing Git you will need to run a couple commands to link it to your github profile. 
> 3. Run the commands in the **Your Identity** [in this link][4]. The same commands are copied below.

```
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

## Fork and Clone this repository
Whenever you are in position to make changes to someone elses project on Github you will need to `fork` the repository and then `clone` it to your local machine. After making changes you will `commit` your work locally and then `push` those changes back to Github where you will finally make a `pull` request so that the new changes may be incorporated into the project.

![git tracking][7]

Let's go through this process now.
> 1. At the very top of this repository, you will see a `Fork` button. Click it and fork the repository. This makes an exact replica of the repository under your user profile.
> 1. Under your Github profile (not mine), again go the top of the page and look for the green `Clone or download` button. Click it and copy the url.
> 1. On your local machine, create a new folder somewhere in your file system. Title it something like `Github Repos` 
> 1. Open up a terminal (Windows users open the program Git Bash)
> 1. `cd` into the new directory you created abovegg

> 1. Run the command `git clone https://github.com/tdpetrou/Intro-to-Data-Science-with-Python.git` but replace this URL with the one you copied from step 2.
> 1. You now have a replica of the repository on your local machine and are ready to make changes
> 1. Staying in the terminal run the command `cd Intro-to-Data-Science-with-Python`
> 1. Open up the README.md file in a text editor. That is this current file.
> 1. Make a single edit to the file and save it. Add your name or something personal on the very top line.
> 1. Go back to the terminal and run the command `git add README.md`. Git is now tracking this file and it is in the staging area.
> 1. Run the command `git commit -m "your message here"`. Replace 'your message here' with something that describes the changes you made. All commits must have a message about what has changed.
> 1. The last command just took a snapshot of your repository and you can revert back to it now at any point in the future.
> 1. Run the command `git push origin master`. This will align your remote repository with your local repository.
> 1. Go back to your github profile and verify the changes.
> 1. Towards the top of the page click the `New pull request` button.
> 1. Now I will get a notification that you are wanting to modify a file of mine. I can review the revisions and accept/reject your pull request.

# Installing Python 3 with Anaconda 
Anaconda is by far the most popular distribution of the Python programming language for data scientists. Anaconda packages together all the popular data science libraries along with the package manager `conda`. 

Anaconda is not a necessity. Python may be installed independently from source from [Python.org][2] along with its own package manager `pip`. But for begninners it is highly suggested to begin with the Anaconda distribution and `conda` command line tool. You can read more about the differences between [Anaconda with conda and pip here][5].

> Visit the [Anaconda downloads page][6] and download Anaconda with Python 3.6 for your operating system. Use the graphical installer. Anaconda comes packaged with a graphical user interface for beginning projects as well as the popular IDE Spyder.

# Run Python Interactively
Now that we have Anaconda installed we can begin to use Python.

> 1. Open up a terminal
> 1. Type in `python` and press enter
> 1. This should open an interactive Python command prompt directly in the terminal. 
> 1. In the first line, you should see that you are running Python 3.6.1 via Anaconda. It should look like this `Python 3.6.1 |Anaconda custom (x86_64)`
> 1. This command prompt is also widely known in computing as a REPL (Read-Evaluate-Print-Loop) - "also known as an interactive toplevel or language shell, is a simple, interactive computer programming environment that takes single user inputs (i.e. single expressions), evaluates them, and returns the result to the user" - [from wiki][12]
> 1. Let's write a few Python commands now

# Using a Text Editor

Interactive programming using the Python REPL is nice to immediately get results together but when building larger programs its likely that you will need a more formidable programming environment such as a text editor. There are [dozens and dozens][13] of text editors. This tutorial covers the popular Sublime Text 3 editor which may be used for any programming language. 

# Installing Sublime Text 3
There are many ways to run and write Python. Python can be written in any text editor, even the basic ones that come preinstalled with all operating systems. Sublime Text 3 is an enhanced text editor that is highly customizable to help make programming in Python easier.

> [Download and install Sublime Text 3][8] and open it.

To enhance the editing experience of sublime specifically for Python we first need to install the package control manager. This is the package control manager for Sublime and has nothing to do with `conda` or `pip`. There are 1000's of third party packages written for Sublime.

> 1. Visit the [Package Control website][9]. All Sublime packages can be found here. 
> 1. Click the `install now` button and follow the instructions to install the package manager.

Now that you have the package manager, you may begin to install packages. We will install the Anaconda Sublime package. This has nothing to do with the Anaconda distribution, it just happens to share the same name. It adds code completion, linting, inline documentation and more. Visit the [Anacond Sublime package home page][10] for more info.

> 1. To access the package manager, you must first open up the `command palette` with `cmd + shift + P`. It is also found under Tools -> Command Palette.
> 1. In the text box that pops up, begin typing in the word `install`. Click on `Package Control: Install Package`
> 1. A new text box will open up with a huge list of available packages
> 1. Type in 'Anaconda'. It should be the first option damnwidget.github.io/anaconda

[Watch this video][11] to get more in-depth tutorial on Sublime packages for Python.

# Opening our first Python program
Open up the program `guess_number.py` in Sublime. This is a small game that attempts to guess your number within 5 steps. Before we play or analyze the game, take a look at the bottom right hand corner of Sublime. You should see some text that reads `Tab Size: 4`. There is nothing inherrently wrong with this except that Python's style guide PEP 8 suggests using 4 spaces over tabs. To change the default settings do the following:

> 1. While in `guess_number.py` click on `Sublime Text -> Preferences -> Settings - Syntax Specific`
> 1. This will open up a file titled `Python.sublime_settings`. 
> 1. Append to the end of this JSON file: `"translate_tabs_to_spaces": true`
> 1. This defaults all tabs to spaces for only your Python files. You might need to close and reopen sublime to see the effects take place.

Now lets take a look at the contents of `guess_number.py`. Comments may be made with the hash symbol or between triple quotes. The top of the file has comments with the author's name and purpose. All functions have triple quotes immediately after their definition. These quotes have a special name and purpose. They are called docstrings and magically appear whenever you attempt to get help on this function in the future.

You should also see different lines of text outlined and some gray circles to the left of the line numbers. This indicates that there might be some linting or style issues with the current code. You can customize the appearance of all your downloaded sublime packages. Go the menu Sublime Text -> Preferences -> Package Settings -> Anaconda -> Settings - Default. This is a JSON file that has easy to read documentation.

Let's change one of the settings in this file. 
> 1. Scroll down to around line 286
> 1. Find the line with the `anaconda_linter_mark_style` setting. It should currently be mapped to `outline`.
> 1. Look at the comments above and change the setting to something else
> 1. Go back to the `guess_number.py` file and notice the changes.

## Executing this program
The most straightforward way to execute this program is to do the following:
> 1. Open a terminal
> 1. `cd` into the directory where `guess_number.py` exits
> 1. Run the command `python guess_number.py`
> 1. Play the game a few times 

## Running programs in Sublime
Some programs may be run directly in Sublime. Unfortunately, `guess_number.py` does not work since it takes user input. We will download an additional package later that will allows us to run it. 

For now we will run a different program by using the build system. 

> 1. Open th file `rain.py`. This program may be found at [matplotlib's site][14].
> 1. Go to Tools -> Build to make it rain
> 1. Exit out of program and press `esc` to remove the bottom window.

## Using the Sublime console
Sublime comes with its own Python interpretter that is separate from the one that you downloaded with the Anaconda distribution.

> 1. Go to View -> Show Console
> 1. Type in some basic Python commands

This is not meant for serious development. There is a much better console that you can add to Sublime.

## SublimeREPL Package
We will now download another very useful package called `SublimeREPL`.

> 1. Open the command pallete with `cmd + shift + p`
> 1. Begin typing in `install` and open the `Package Control: Install Package`
> 1. You will see a very long list of available packages
> 1. Type in `SublimeREPL` and install it.
> 1. Open up the command pallete again and type in `SublimeREPL: Python` and press enter
> 1. This runs the REPL directly in Sublime
> 1. Run a few Python commands

### Running `guess_number.py` with SublimeREPL
Remember how I mentioned above that `guess_number.py` does not run well by using `Build`? You can however, run the program with SublimeREPL.

> 1. Go to the `guess_number.py` file
> 1. Go to Tools -> SublimeREPL -> Python - Run Current File 
> 1. This exacat option is also available via the command palette.



Sublime has a [very detailed documentation][15] page where you can learn everything about it.

pycharm
https://www.jetbrains.com/pycharm-edu/
file -> new project -> educational
choose python 3 interpreter

use jupyter notebook in pycharm: https://www.jetbrains.com/help/pycharm/using-ipython-jupyter-notebook-with-pycharm.html


Typical workflows for data scientists

[1]: (https://www.meetup.com/Houston-Data-Science/) 
[2]: (https://www.python.org/downloads/)
[3]: https://git-scm.com/downloads
[4]: https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup
[5]: https://jakevdp.github.io/blog/2016/08/25/conda-myths-and-misconceptions/
[6]: https://www.continuum.io/downloads
[7]: https://prismoskills.appspot.com/lessons/Git/imgs/git_file_stages.png
[8]: https://www.sublimetext.com/
[9]: https://packagecontrol.io/
[10]: http://damnwidget.github.io/anaconda
[11]: https://www.youtube.com/watch?v=xFciV6Ew5r4
[12]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop
[13]: https://en.wikipedia.org/wiki/Comparison_of_text_editors
[14]: https://matplotlib.org/examples/animation/rain.html
[15]: http://docs.sublimetext.info/en/latest/
