# simple-flask-app

## Disclaimer

The installation of packages and modules done here worked on my own system. There is no guarantee that these steps and fixes will work for your system. As with any new software, make sure you understand the commands you intend to execute before pressing `ENTER`. Proceed with caution!

## Setup

Below are the steps I followed to set up this project. The steps may differ for you.

Assuming you have `pip`, if you have not set up `virtualenv` and `virtualenvwrapper` you should do the pre-install!

### Pre-Install

1. `pip install virtualenv`
2. `pip install virtualenvwrapper`
3. From root `mkdir ~/.virtualenvs`
4. Open `.bashrc`
5. Include `export WORKON_HOME=~/.virtualenvs` and `/usr/local/bin/virtualenvwrapper.sh`
6. Save then close and re-open terminal.

### Install

1. `mkdir simple_flask_app` OR `git clone <REPO URL>`
2. Check the path for python3 `which python3`
3. Create a virtualenv with python3 path in the flag `mkvirtualenv --python=<PYTHON PATH> <VIRTUAL ENV NAME || py_env>`
4. Check that virtual env has been created `ls -l ~/.virtualenvs/`

### Errors

In my limited experience, installing things Python-related has a 50/50 chance of returning a traceback error. Here are the issues I have come across in this project:

1. Installing virtualenvwrapper throws a traceback error involving `six-1.4.1`

This seems to be a problem with your computer if you are running OSX. To solve this:

`sudo pip install pbr`
`sudo pip install --no-deps stevedore`
`sudo pip install --no-deps virtualenvwrapper`

[Can't install virtualenvwrapper](https://stackoverflow.com/questions/32086631/cant-install-virtualenvwrapper-on-osx-10-11-el-capitan)

## Resources
- [How to Use Virtual Environments for Python Projects](http://www.patricksoftwareblog.com/how-to-use-virtual-environments-for-python-projects/)
- [Creating a Simple Flask Web Application](http://www.patricksoftwareblog.com/creating-a-simple-flask-web-application/)