# Module Assessments and Instructions

## Introduction

Towards the end of each phase of this course, you'll receive an assessment in
the form of a code challenge. This code challenge is a chance for you to show
off how much you've learned, see where you are in terms of grasping the
material, and get feedback from us on ways to improve or areas to work on
further.

The first challenge will cover your knowledge of JavaScript and frontend
development. Topics will include DOM manipulation, event handling, and
communicating with a server.

For the first code challenge, you'll receive a repo with instructions and
deliverables. For example, one deliverable might be "As a user, I should be able
to add a comment to a blog post". It's an open-book, totally Googleable
challenge. As opposed to standard labs, there will not be tests. Instead, we
will be reading, running, and grading your code based on how you fulfill the
requirements and your use of coding best practices. We will give you
constructive feedback based on your submission.

You can expect feedback after we grade your submission. We'll set aside time for
each of you over the subsequent week to review if you don't pass the challenge.

Future code challenge assessments will follow a similar format, but of course,
the topics will be different. You can expect any of the topics we cover in class
to be touched on in some way. The best way to prepare will be to consistently
complete labs, review your lecture notes, and build your own projects.

Please don't think of passing the assessments as the goal of your learning —
doing well on them should be a side effect, a by-product of you learning how to
be an amazing developer. By all means, get more practice in any areas where you
know you need it, but don't cram for a code challenge, and definitely don't
sacrifice keeping up with the labs to prepare for it.

Below, we've provided instructions for how to work on and submit your future
code challenges. This lesson is structured the same way they will be, so feel
free to practice here.

## Installing Python

Before you can start working on a code challenge, you must check if you have
Python installed on your system.

While you do not need to know or write any Python code to solve these
challenges, you will be running provided Python scripts to start the challenge.

To check if you have Python installed, open up the terminal and run the command:
`python --version`.

If you receive output telling you what version of Python you have, such as:

```bash
$ python --version
> Python 3.8.13
```

This means you already have Python installed. You can skip the rest of this
section and move onto the "Instructions for Working on and Submitting Code
Chllenge" section.

If you receive anything other than a Python version, continue through the
appropriate installation steps below.

## Installing Python on MacOS

Before installing Python, we first need to install `pyenv`, a version manager
for Python. We will likely only use Python version 3.8.13 in the Software
Engineering curriculum, but installing pyenv will make it simple to install
newer versions later on.

Enter the following command in the Terminal:

```console
$ brew install pyenv
```

Open your shell startup file (either `.zshrc` or `.bash_profile`) with the
following command:

```console
$ code ~/.zshrc
```

or

```console
$ code ~/.bash_profile
```

Add the following to the end of the file:

```text
if which pyenv > /dev/null; then
  eval "$(pyenv init -)";
fi
```

We want to load `pyenv` every time we open a new terminal window; this will make
sure that it does! Enter the following command to load your new settings:

```console
$ source ~/.zshrc
```

or

```console
$ source ~/.bash_profile
```

With `pyenv` installed, we can now install Python.

Run the following command to install Python (you'll notice pyenv makes us put in
the exact version instead of being able to just say 3.8 or 3):

```console
$ pyenv install 3.8.13
```

After some time this should complete without any errors. It could take a while
since you are compiling Python from source code.

Once this is finished we also need to tell pyenv this is our default version of
Python using this command:

```console
$ pyenv global 3.8.13
```

Ensure that these changes take effect by closing your terminal and opening a new
one.

You can verify that you have the correct version of Python installed by typing:

```console
$ python3 --version
```

This command should show 3.8.13.

## Installing Python on WSL2

**Note**: We do not install Python using the installer from python.org in our
curriculum. If you have installed Python using this tool, you should uninstall
it before installing this version of Python.

Currently the curriculum for this course is compatible with Python 3.8.

**Installing pyenv**

Before installing Python, we need to install the Python version manager pyenv.
This is similar to the nvm tool we used to install Node.JS, except it controls
which versions of Python we use on our system.

To install pyenv, we use the [pyenv-installer][].

Per the instructions on the [pyenv-installer][] website, we start by running the
following command:

```console
$ curl https://pyenv.run | bash
```

[pyenv-installer]: https://github.com/pyenv/pyenv-installer

Unlike nvm, pyenv does not automatically add its startup lines to your shell
startup file.

The files that you have to change will depend on which shell you are running
(you can check which shell you have by running echo $SHELL). Follow the
instructions to update the startup files associated with the shell that you are
running.

Open your `.zshrc` or `.bashrc` file with the following command:

```console
$ code ~/.zshrc
```

or

```console
$ code ~/.bashrc
```

Add the following lines:

```text
export PYENV_ROOT="$HOME/.pyenv"
export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init --path)"
```

To get your startup file to execute, restart your terminal.

**Installing Dependencies on Windows and Ubuntu**

For Windows and Ubuntu users you will need to install some extra dependencies
for Python. (See here for more information about the prerequisites: pyenv
Prerequisites)

First run this command to update your apt repositories:

```console
$ sudo apt update
```

Next, run this command to install the packages listed on the pyenv:

```console
$ sudo apt-get install -y build-essential libssl-dev zlib1g-dev libbz2-dev \
libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev \
xz-utils tk-dev libffi-dev liblzma-dev python-openssl git
```

**Installing Python**

With `pyenv` and other dependencies installed, we can now install Python.

Run the following command to install Python (you'll notice pyenv makes us put in
the exact version instead of being able to just say 3.8 or 3):

```console
$ pyenv install 3.8.13
```

After some time this should complete without any errors. It could take a while
since you are compiling Python from source code.

Once this is finished we also need to tell pyenv this is our default version of
Python using this command:

```console
$ pyenv global 3.8.13
```

Ensure that these changes take effect by closing your terminal and opening a new
one.

You can verify that you have the correct version of Python installed by typing:

```console
$ python --version
$ python3 --version
```

Both of these commands should show 3.8.13

## Instructions for Working on and Submitting Code Challenge

When a code challenge is published, it will be available in the Code Challenges
module of this course.

Once it's available, you must start the code challenge by following the steps
below:

- Find and open the code challenge assignment in Canvas and download the linked
  ZIP file
- Unzip the file on your computer
- In your terminal, change directory (`cd`) into the unzipped challenge
  directory
- Run `ls`; you should see a `bin/` directory and a `code-challenge.bundle`
  file)
- Run `./bin/start <your-name>` from the directory; this will create a new
  directory called `code-challenge/`
- `cd` into the new `code-challenge/` directory and open it in your code editor

To work on your code challenge:

- Ensure that you're in the `code-challenge/` directory
- Follow the instructions in the `README.md` file
- `git add .` and `git commit` inside of the `code-challenge/` directory often
  as you're working

To submit the code challenge:

- Navigate to the **parent directory** of `code-challenge/` in your terminal
- Run `./bin/end`, which will create a new file, `<your-name>.bundle` in that
  directory (for example, `alicia.bundle`)
- Navigate back to the code challenge assignment in Canvas
- Upload `<your-name>.bundle` to the assignment and submit

**Reach out to your instructors immediately** if you run into issues
downloading, working on, or uploading your code challenge.
