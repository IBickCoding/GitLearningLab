# Creating and Understanding Repositories

## Learning Objectives:

At the completion of this lesson, learners will be able to:

1.  Define what a Git repository is.

2.  Explain the purpose of a repository.

3.  Identify the basic structure of a repository.

4.  Differentiate between a local and remote repository at the basic
    level.

------------------------------------------------------------------------

## Introduction

At one point or another in our learning careers we have been tasked with
completing a project that uses one or more files. Wouldn't it be cool if
there was a piece of software that helped you manage those files and
their history?

Perhaps you were working on a Microsoft Word document for this
hypothetical project. You include a section that you thought would be
great for your topic and support that section by making changes to other
areas of your project to get a better flow into your newly included
ideas. Everything is great until you have someone read your document and
they tell you that information is incorrect and you have now structured
your project around that one idea.

Do we go through the entire document and remove the changes you made to
perfectly good sections just to root out the bad information? What if
you miss some of the changes that you made and you make the document
worse because you now have information that leads to sections that no
longer exist?

Git solves this problem. Since Git is a version control system, we can
save snapshots of how our files looked prior to certain changes made.
This means we can just revert to a commit before we made the bad
changes. Think of it like a time machine to take us back to better
times.

But we are getting ahead of ourselves. Before learning about how Git
tracks those changes, we need to understand what a repository is and how
we create one.

![](./media/UnderstandingRepositories/media/image1.gif){width="2.40625in"
height="1.6813549868766404in"}

## What is a Repository?

A repository (very often referred to as a "repo") is a storage location
where Git tracks files, folders, and a history of changes made to all
files and folders within itself.

We can think of a repository as a filing cabinet like we explained
before. Essentially, each project becomes its own filing cabinet where
we can place folders inside of each drawer. In each of those folders, we
may have more folders or files within the folders. We may even have
loose files inside the filing cabinet drawer.

Within each of these folders and/or files, we also have a history record
attached. This allows us to see who has made what changes and when!

A repository at its core contains:

- Project files and folders

- Git tracking information

- Commit history

- Configuration data

## Understanding Local Repositories

A local repository exists on your computer and your computer only. When
you create a repository using Git, all files and history are stored on
your computer.

This may seem like a waste of time but there are a few benefits from a
local repository that are not immediately obvious. As we explained in
the introduction, reverting to a previous version of a file is very
handy but this is not the only benefit.

- Fast access to tracked files.

- No internet required.

- Safe experimentation when making changes to files.

- Private development that cannot be viewed by others.

## Understanding Remote Repositories

A remote repository on the other hand is a copy of your local repository
on another system. Typically, remote repositories are hosted on a cloud
hosting website such as GitHub, Bitbucket, or equivalents.

However, just because your repository is being hosted somewhere else
does not mean that anyone can access it. There are 2 main privacy
options for a remote repository which are public and private.

Private repositories only give access to the contained files to the
owner of the repository and anyone that owner gives permission to access
the files. This means we could use a remote repository to share files
privately with other people that may be working with us from anywhere in
the world.

Public repositories give access to anyone that finds the repository. The
Git Learning Lab is a public repository, meaning that anyone that finds
it can access the files contained within it. Public "repos" are a way to
be able to disperse information to a lot of people if privacy is not a
concern.

It is important to note though that just because a remote repository is
a copy of a local repository, it does not mean that making changes to
one automatically makes changes to the other. We must explicitly bridge
the gap of communication between Git and the hosting platform. Right
now, we do not need to worry about that and instead just understand the
two concepts.

Benefits of a remote repository include:

- Easy collaboration and sharing of ideas or files.

- Backup and recovery options.

- Access from multiple devices that are not geographically tied to each
  other.

- Centralized project management.

![](./media/UnderstandingRepositories/media/image2.gif){width="2.5in"
height="1.8661975065616798in"}

## Quick Recap of Local Repository vs Remote Repository

  -----------------------------------------------------------------------
  **Local Repository**                **Remote Repository**
  ----------------------------------- -----------------------------------
  Stored on your system               Stored on another system

  Works without internet              Requires internet access

  Used for private development        Used for collaborative development
                                      or public distribution

  Private by default                  Can be shared with others or not.
  -----------------------------------------------------------------------
