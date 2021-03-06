# simple-flask-app

## Purpose

The purpose of this project is to improve on my current Python skills. I will be using `pip` as my package manager, a virtual environment builder `virtualenv`, and the microframework [Flask](https://github.com/pallets/flask).

## Disclaimer

The installation of packages and modules done here worked on my own system. There is no guarantee that these steps and fixes will work for your system. As with any new software, make sure you understand the commands you intend to execute before pressing `ENTER`. Proceed with caution!

## Setup

Below are the steps I followed to set up this project. The steps may differ for you.

Assuming you have `pip3`, if you have not set up `virtualenv` and `virtualenvwrapper` you should do the pre-install!

### Pre-Install

*you may need to use `sudo` to run these commands successfully*

1. `pip install virtualenv`
1. `pip install virtualenvwrapper`
1. `mkdir ~/.virtualenvs`
1. Open or `touch .bashrc` then open `.bashrc`
1. Include in your `.bashrc`
```bash
export WORKON_HOME=~/.virtualenvs
/usr/local/bin/virtualenvwrapper.sh
```
6. Save then close and re-open terminal.

### Install

1. `git clone REPO_URL`
1. `cd` into folder
1. Check the PYTHON3_PATH for python3 
```bash
which python3
```
4. Create virtual environment with your custom unique VIRTUALENV_NAME name or use py_env if you haven't before
```bash
mkvirtualenv --python=PYTHON3_PATH VIRTUALENV_NAME
```
5. Check that virtual environment has been created 
```bash
ls -l ~/.virtualenvs/
```
6. Activate the virtual environment 
```bash
workon VIRTUALENV_NAME || py_env
```
7. `pip install -r requirements.txt`
8. `python run.py`
9. Open your browser to `localhost:5000`
10. TA DA!

## Errors

In my limited experience, installing things Python-related has a 50/50 chance of returning an error. Here are the issues I have come across in this project:

[Can't install virtualenvwrapper](https://stackoverflow.com/questions/32086631/cant-install-virtualenvwrapper-on-osx-10-11-el-capitan)

Installing virtualenvwrapper throws a traceback error involving `six-1.4.1`. This seems to be a problem with your computer if you are running OSX. To solve this:

1. `sudo pip install pbr`
1. `sudo pip install --no-deps stevedore`
1. `sudo pip install --no-deps virtualenvwrapper`

## Resources
- [How to Use Virtual Environments for Python Projects](http://www.patricksoftwareblog.com/how-to-use-virtual-environments-for-python-projects/)
- [Creating a Simple Flask Web Application](http://www.patricksoftwareblog.com/creating-a-simple-flask-web-application/)
