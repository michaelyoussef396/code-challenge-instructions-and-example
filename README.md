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
section and move onto the section below.

If you receive anything other than a Python version, refer to the Python
installation lessons for your OS in this Code Challenge module.

Once you've successfully installed Python, you can continue to the section
below.

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
