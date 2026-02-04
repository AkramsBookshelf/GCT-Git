# 📜 GIT For Game Development
> By: Akram Taghavi-Burris | © 2026

Now that we've discussed the importance of **[!version control systems (VCS)](VersionControl.md)** and why Git is one of the best solutions for beginners, we need to get it ready for action. Before we even open a game development project, we must set up our environment. Understanding version control in theory is one thing, but mastering the ecosystem is what separates a hobbyist from a professional developer. Especially in game development, where high-res textures and 3D models can easily break a standard repository, knowing how to configure your tools correctly from day one is the difference between a smooth workflow and a corrupted project. In this lesson, we will install the essential toolkit and configure your environment to handle everything from simple scripts to massive game assets.

## Git Vs GitHub

As a beginner, you might often hear **Git** and **GitHub** used interchangeably, but it’s important to make the distinction that they are not the same.

**Git** is a version control application that **must be installed on your computer to function**. It lives locally on your machine and allows you to track changes to your project over time by creating snapshots (called _commits_). If something breaks, Git acts as your safety net, letting you look back at earlier versions or restore previous states of your project.

**GitHub**, on the other hand, is a cloud service. It stores your Git repositories online so they can be backed up, shared, and accessed remotely. Think of GitHub as the "cloud home" for the work you create using the Git application.

Before we can implement Git version control in our projects, we first need to ensure the application is installed on our local computers.

>[!IMPORTANT]
> For Windows users, installing Git also installs a tool called **Git Bash**. Git was originally created for Linux systems; as such, Windows needs a "translator" to run certain commands. **Git Bash** is a terminal window that provides this environment, allowing you to use Git exactly like professional developers do on Mac or Linux.


>[!NOTE]
> If you are working in a classroom computer environment, the Git application should already be pre-installed.
> You can skip the download step in the following tutorial and move straight to Step 2: Verifying Your Installation.

---

## 🛠️ TUTORIAL: Installing Git

<details>
<summary><strong><em>Tutorial Details</em></strong></summary>

|📝 Topic          | 🕑 Estimated Time | 🧰 Requirements   |
| :---------------: | :---------------: | :---------------: |
| Project Managment | 5 minutes        |       |

</details>

#### Step 1: Download and Install Git

If you are working on your personal laptop or home computer:

1.  Download: Visit the official Git website: 👉 **[https://git-scm.com/](https://git-scm.com/)**
2.  Install: Run the installer. You will see several configuration screens—for this course, it is recommended to keep the default settings and click "Next" through the prompts.
3.  Finish: Once the installation is complete, the Git "engine" is ready to go.
    

#### Step 2: Verifying Your Installation

To confirm the application is correctly installed, let's try opening your new terminal:

1.  Windows: Search your Start Menu for Git Bash and open it.
  - Mac: Open your standard Terminal.  
2.  Type `git --version` and press Enter.
4.  Success: If you see `git version 2.x.x`, the application is active and ready.

---

## Git LFS for Game Development

While Git is perfect for tracking thousands of lines of code, it wasn't originally designed for the high-fidelity assets we use in game engines. A single game development project may include hundreds (if not more) large binary files, such as:

-   .fbx models
-   Textures (4K, normal maps, etc.)
-   Audio files (.wav, .mp3)

If you try to store these directly in a standard Git repository, your project will eventually become so "heavy" that it becomes impossible to download or sync. This is where **Git Large File Storage (Git LFS)** comes in.

**Git LFS** is an extension to Git that handles large files more efficiently. Instead of storing large files directly in your repository history, Git LFS replaces them with tiny "pointer" files and stores the actual heavy data separately. This keeps your repository lightweight and manageable, no matter how many 3D models you add.

>[!NOTE]
> Like Git, Git LFS should already be active on classroom computers. You can verify this by skipping to Step 2: Verifying Your Git LFS Installation in the tutorial below.

### Local vs. Cloud Storage
While installing and using Git LFS locally is a perfect solution for managing your game project on your own machine, you may run into restrictions once you connect to **GitHub**. Although the Git LFS tool itself is free to use, GitHub's cloud storage is not unlimited.

For independent developers and students working on small-scale projects, GitHub's free tier is often sufficient. However, you should be aware of the following professional constraints:

-   **1GB Limit**: On a personal free GitHub account, you are typically limited to 1GB of LFS storage. In game development, you can hit this limit surprisingly quickly with just a few high-resolution textures, 3D models, or high-quality audio stems.
    
-   **Bandwidth Caps**: GitHub also tracks "bandwidth"—the amount of data transferred when you or a teammate downloads (clones/pulls) your project. If your project is large, you might run out of download "credits" before the month is over.
    
-   **Sync Block**: Once you hit these limits, GitHub will stop accepting your Pushes. While you can still work locally on your computer, you won't be able to back up your work or submit assignments online until the storage is cleared or your account is upgraded.
    

> [!NOTE]
> Most educational institutions utilize a GitHub Education license. This provides significantly more LFS storage and bandwidth, but there is a catch: it only applies if your project is hosted within the school’s official GitHub Organization.
> Always use the provided GitHub Classroom links for your assignments to ensure you stay within the school's professional storage quota.

---

## 🛠️ TUTORIAL: Installing Git

<details>
<summary><strong><em>Tutorial Details</em></strong></summary>

|📝 Topic          | 🕑 Estimated Time | 🧰 Requirements   |
| :---------------: | :---------------: | :---------------: |
| Project Managment | 5 minutes        | Git        |

</details>

#### Step 1: Download and Install Git LFS
1.  Download: Visit the official Git LFS website: 👉 **[https://git-lfs.com/](https://git-lfs.com/)**
2.  Install: Run the installer on your computer.

#### Step 2: Verifying Your Git LFS Installation
1.  Windows: Search your Start Menu for Git Bash and open it.
  - Mac: Open your standard Terminal.  
2.  Type `git lfs install` and press Enter.
3.  Success: If you see `Git LFS initialized.`
    
---
## 

### Command Line vs. GUI Tools

Git was originally designed to be used from the **command line**, using tools like Git Bash. This method is incredibly powerful, but it requires you to be familiar with specific text-based commands to manage your project. While many professional developers still prefer the terminal, it can be a steep learning curve when you are also trying to learn game development.

If you aren't comfortable working in a terminal yet, that’s completely fine. Once Git is installed, you can use a **Git GUI (Graphical User Interface)**.

A popular option is **GitHub Desktop**, which provides a visual way to manage your commits, branches, and syncing without typing commands. It allows you to see your changes and history at a glance, making it much easier to keep track of complex game projects.

> [!TIP]
> While tools like GitHub Desktop provide excellent GUI support for your daily workflow, some complex Git features or "emergency" fixes will still require the command line.

--- 
## 🛠️ TUTORIAL: Installing GitHub Desktop

<details>
<summary><strong><em>Tutorial Details</em></strong></summary>

|📝 Topic          | 🕑 Estimated Time | 🧰 Requirements   |
| :---------------: | :---------------: | :---------------: |
| Project Managment | 5 minutes        | Git, Git LFS       |

</details>

#### Step 1: Download and Install GitHub Desktop
1.  Download: Head to the official download page: 👉 **[https://desktop.github.com/](https://desktop.github.com/)**
2.  Run the Installer: Once the download finishes, run the setup file.
3.  Launch: On Windows, the app will usually open automatically after installation.
    - On Mac, drag the GitHub Desktop icon into your Applications folder and launch it from there.

#### Step 2: Sign In and Authenticate
1.  Click the **`Sign in to GitHub.com`** button on the **welcome screen**.
2.  This will open your default web browser. Log in to your **GitHub account**.
3.  Click the green **`Authorize desktop`** button.
   - Your browser may ask for permission to _Open GitHub Desktop_; click Allow or Open.
    
#### Step 3: Configure Your Git Identity
After signing in, the app will **ask for your Git Config details** (Name and Email).
-   The Rule: Use the same name and email associated with your GitHub account.
    - This information is attached to every "snapshot" (commit) you make. It records exactly who authored the changes in the project.
-   Select **`Use my GitHub account settings`** to ensure they stay perfectly synced.

#### Step 4: Final Verification
To ensure your account is correctly linked for our class:
1.  In GitHub Desktop, go to **File > Options (Windows)** 
    - Or **GitHub Desktop > Settings** (Mac).
2.  Click on the Accounts tab.
3.  Check your status: You should see your GitHub username and avatar.

   
    

> \[!IMPORTANT\] Check Your Account: If you see a different username, you must sign out and sign back in using the specific account you used to join our GitHub Classroom organization. If the accounts don't match, you won't be able to see or submit your assignments!
