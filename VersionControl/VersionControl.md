# 📜 Version Control 
> By: Akram Taghavi-Burris | © 2026

As a development project grows, it becomes harder to keep track of what’s changing, why it changed, and who changed it. Early on, when you’re working alone and only have a few scripts, you can often get away with manually saving backups or making copies of your project folder. But as more systems are added, and especially as more people join the team, this quickly becomes risky. A single fatal bug, a corrupted project file, or even a server crash can wipe out not just hours of work, but potentially months or years of progress. Professional teams avoid this by using tools designed specifically to track project history, recover from mistakes, and protect the project from unexpected disasters. One of the most important of these tools is version control.


## What Is Version Control?

A **Version Control System (VCS)** is a tool that tracks changes in a project over time.

In the early days of software development, this was often called **source control** because projects were mostly composed of code (source files). But modern game projects contain far more than scripts:

-   Images
-   Audio
-   Animations
-   3D models
-   Materials and textures
-   UI layouts
-   Level files
-   Prefabs and configuration data
    

So the term expanded into **version control**, because we’re now tracking _everything_, not just source code.

Instead of trying to manage file history manually, a VCS stores a complete timeline of your project, allowing you to:

-   Save meaningful checkpoints (called **commits**)
-   Undo mistakes safely
-   Collaborate with others without overwriting work
-   Experiment without risking the main project

---  

## Version Control as a Multiverse

A great way to picture version control is through the lens of the multiverse, similar to how it’s portrayed in Marvel’s _Loki_.

In the show, the “sacred timeline” represents the main reality. Branching timelines represent alternate versions of events where different choices were made.

A VCS works the same way.

![Version Control: Naviagting the Project Multiverse](imgs/gct-versionControl.png)

# 

### Repository = The Universe

A project lives inside a **repository** (or **repo**).  
A repo contains:

-   All files in the project
-   The full history of changes
-   The branching structure of the project timeline
    
# 

### Main Branch = The Sacred Timeline

Your **main branch** represents the “official” version of your project.

Every time you **commit**, you’re saving a snapshot of your project at a moment in time. This creates a timeline you can return to whenever you need.

#

### Branches = Alternate Realities

The real multiverse appears when you create a **branch**.
A branch is an alternate timeline where you can:

-   Test a new feature
-   Try a risky experiment
-   Fix a bug
-   Work on a new level    
-   Redesign a system

…without touching the main timeline.

#

If your experiment works, you **merge** the branch back into main.  
If it fails, you discard the branch and the sacred timeline remains untouched.

---

## Why Use Version Control (Even Solo)?

A lot of beginners assume "version control is only for big teams"; It’s not!

Even as a solo developer, version control is one of the most valuable tools you can learn because it gives you:

-   A reliable project backup system
-   A way to undo mistakes without panic
-   A history of what changed and why
-   A safe way to experiment using branches
    
And there’s a second reason that matters just as much: **Version control is an industry expectation.**

Even entry-level game development roles often list version control experience as a requirement, because professional development workflows depend on it.

---

## Core Version Control Concepts

Before we look at different VCS tools, it helps to understand the vocabulary most systems share.

### Commit

A **commit** is a saved checkpoint in your project history.

A commit typically includes:

-   The files that changed
-   The exact differences
-   A message describing why the change was made
    
#

### Branch

A **branch** is an alternate timeline of the project.

#

### Merge

A **merge** is the process of combining one branch back into another.

#

### Repository (Repo)

A container that holds:

-   the project files
-   the version history
-   the branches
    
---

## Centralized vs Distributed Version Control

Version control systems generally fall into **two models**:

-   **Centralized systems**
-   **Distributed systems**
    

Both use a repo and both track history, but the way they store and synchronize that history is different.

### Centralized Version Control

In a **centralized** VCS:

-   There is one main repository on a server
-   Developers connect to that server
-   The server is the “source of truth.”
    

A common workflow looks like this:

1.  Developer gets the latest project files
2.  Developer checks out a file (often locking it)
3.  Developer edits the file
4.  Developer checks in the file (sends changes back to the server)
    

#### Why centralized systems are popular in games

Games contain lots of **large binary assets** (like textures, models, audio). These files do not merge well.

Centralized VCS systems often support file locking, meaning:

> Only one person can edit a file at a time.

That prevents conflicts like two artists editing the same 3D model and overwriting each other.

#

### Distributed Version Control

In a **distributed** VCS:

-   Each developer has a full copy of the repo
-   Each copy contains the full history
-   Commits happen locally first
-   Changes are later synchronized back to the main repo
    

A common workflow looks like this:

1.  Clone the repository
2.  Work locally
3.  Commit changes locally
4.  Push changes to the shared server repo
5.  Pull other people’s updates
    

#### Why distributed systems are popular in software

Distributed VCS tools are:

-   Fast
-   Flexible
-   Great for code-heavy projects
-   Good for experimentation
-   Usable even while offline
    

#### One drawback

Because each clone contains the full history, large repos can take up significant space.

This becomes especially noticeable in game projects with large assets.

#

## Popular Version Control Tools

Now that we understand the purpose and structure of version control, let’s look at the most common tools used in game development.

## 🧰 Git (Most Popular Overall)

**Git** is the most widely used version control system in the world.

It’s:

-   Distributed
-   Free and open-source
-   Excellent for text-based projects (especially code)
    

Git is often paired with **GitHub**, which provides cloud hosting for Git repositories.

Even though Git is traditionally command-line based, most developers use one of these workflows:

-   Git in the terminal
-   GitHub web interface
-   GitHub Desktop (GUI-based Git workflow)
    

### Git and Game Assets

Git is not designed for large binary files.

However, many indie developers still use it because it’s accessible and widely supported.

To help with large assets, Git can use **Git LFS (Large File Storage)**, which replaces large file history with lightweight pointers.

#

## 🏭 Perforce P4 (Industry Standard for Studios)

The game industry standard for large studios is **Perforce P4** (formerly Helix Core).

It was built specifically for:

-   Large projects
-   Large binary assets
-   High-performance team collaboration
    

Perforce is typically used in a centralized workflow, which makes it easier to:

-   lock files
-   prevent asset conflicts
-   manage huge repositories efficiently
    

### The tradeoff

Perforce is enterprise software.

That means:

-   licensing costs
-   setup complexity
-   a steeper learning curve
    
#

## 🎮 Unity Version Control (Built for Game Workflows)

Unity also offers its own tool: **Unity Version Control**.

It supports workflows that resemble both centralized and distributed models, and it integrates nicely into Unity’s editor.

### The tradeoff

Unity VCS is convenient, but:

-   the free tier is limited
-   it’s less common in the industry than Git or Perforce
-   many studios still expect Git or Perforce experience

---  

>[!TIP]
> #### What Should Beginners Use?
> If you’re learning game development, **start with Git**.
> It’s:
> - free
> - easy to access
> - widely used
> - excellent for building professional habits
>
> Later, if you want to work in larger studios, learning **Perforce P4** is extremely valuable.
> Knowing both makes you more flexible—and much more employable.

---

## 🛡️ Checkpoint

Here are the key takeaways from this lesson:

-   **Version control** tracks the history of a project over time, including code and game assets.
-   A **repository** contains the full project and its complete timeline of changes.
-   A **commit** is a saved snapshot that you can return to later.
-   A **branch** is an alternate timeline where you can experiment safely.
-   **Merging** combines work from one branch into another.
-   Version control is valuable even for solo developers because it acts as a backup system and supports safe experimentation.
-   VCS tools come in two major models:
    -   **Centralized VCS**: one main server repo, often supports file locking (great for large assets)
    -   **Distributed VCS**: each developer has a full clone, commits locally, syncs later (great for code workflows)
-   The most common tools in game development are:
    -   **Git** (most popular overall)
    -   **Perforce P4** (industry standard for large studios)

    -   **Unity Version Control** (integrated, but less widely adopted)


