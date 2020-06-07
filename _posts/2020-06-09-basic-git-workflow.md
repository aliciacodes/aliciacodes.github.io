---
layout: post
title:  "Basic Git Workflow"
date:   2020-06-09
categories: codecademy
---

Today's Day 4 of the Computer Science Path. Right now, I'm in the second part of the Development Skills module in Basic Git Workflows.

In this section, there is one lesson, two projects, a quiz, and two articles. Down below, I will summarize the lesson and the two projects. The articles are teaching the user how to get set up with Github and I will link them down below. 

# Git Workflow Notes
In this section, we learned about Git. Git tracks changes you make to a project, stores the change, and will reference that change when needed.

There are three parts to every project:
1. A Working Directory: All the creating, editing, deleting, and organizing of files happens here.
2. A Staging Directory: Lists changes made to working directory.
3. Repository: Git stores changes permanently and creates a new version or revision of the project.

The typical workflow of a Git project goes like this:
1. Edit a file in the working (current) directory
2. You add files to the staging area
3. Saving changes to a Git repo using commits. 

During this section, six commands were learned to master this system.
<ul>
    <li> git init - Turns current directory into a Git project and you can start tracking changes.</li>
    <li> git status - See whether files are added (committed) to Git or not in the staging directory.</li>
    <li> git add filename - Adds files from staging to working directory.</li>
    <li> git diff filename - shows difference between working and staging area. In the output, if there is a `+` and green text then tat means there is a change to the file. If the text is red that means it is untracked and needs to be commited if you want to add the repository.</li>
    <li> git commit -m "Commit message" - Stores file changes from staging area and moves it to your repository. You must have a commit message and with these messages, you must put it in quotation marks, write it in the present tense, and should be 50 characters or less.</li>
    <li>git log - Lists all previous changes. In the output, there should be a 40-character code, called a SHA that identifies the commit. Then the commit author, date and time, and the message is displayed.</li>
</ul>    

# The Projects and Quiz
In this section, there were two projects. The first, the Manhattan Zoo only dealt with one text file. In this project, you initialized a git repository (`git init`), checked the status (`git status`), and edited a text file that contained meal regiments for the zoo animals. In Git, it is important to note that once a text file is edited you must add it to the staging area again (using `git add filename`) and then you can commit again (using the structure `git commit -m "put anything here`). Once you add, you can check the status again using `git status`. After commiting, you can look at the most recent commit using `git log`.

In the next project, it was much of the same except there were multiple files in the working directory. It is pretty much the same as the Manhattan Zoo. To add multiple files, you can use `git add .` and then commit like you did before.

The quiz was much the same. There were questions like "What does the command `git status` show?" and "What is a `commit`?"

# Articles
<a href = "https://www.codecademy.com/articles/f1-u3-git-setup">Here</a> is a link of how to setup your computer with Git and a Github account!

# Free Alternatives
Since this is a pro module, you cannot learn this material on Codecademy without shelling out $240. I would recommend reading the chapter 2.1 and 2.2 of <a href = "https://git-scm.com/book/en/v2">Pro Git</a>. It goes even more in-depth than this Codecademy module and is incredibly useful. In order to learn these materials, I would recommend making your own flashcards and using Github and Git. While you are learning, use this <a href = "https://education.github.com/git-cheat-sheet-education.pdf">cheatsheet</a>. 