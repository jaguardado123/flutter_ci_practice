# Flutter Continuous Integration (CI) Practice

This is not a homework nor exercise assignment. The purpose of this repo is so that you can follow along with in-class examples without having to install Flutter in your personal computer.

## Basic Setup (Skip if familiar with)

You need to follow the steps below to be able to run your Flutter application.

### Install Extensions and Dependencies

First, install the `Dart` and `Flutter` extensions in Visual Studio Code.

Next, install the necessary Flutter dependencies by running the command below in your terminal.

```
flutter pub get
```

### Run the App

To run your Flutter applications, you need to run the `run.sh` bash script. Use the command below in your terminal.

```
./run.sh
```

### View the App in Browser

Open the **Ports** tab in your bottom screen (where your terminal is). Change the visibility of port `3000` to **public**, then right-click on the URL and select **Open in Browser**.

<br>

## Let's Get Started!

Let's practice using <span style="color: #0096FF">**Continuous Integration (CI)**</span> when updating our GitHub repository. CI is one of the 2 phases of **DevOps** and it focuses on updating your source code to prevent Regression.

<img src="https://github.com/jaguardado123/hangman/blob/main/screenshots/devops.PNG" width="350px">

The first step of CI is to setup your **Configuration-as-Code (CaC)**, this step is where you configure your code repository to enforce the CI pipeline.

### Configuration-as-Code

**1. Require Testing:**

- Your current repository already has a `.github/workflows/flutter_test.yaml` file that tells GitHub Actions to run all of the tests when a Pull Request is made.

**2. Require Code Review:**

- Your current repository also has a `pull_request_template.md` file where you and your team must put a description of your Pull Request. (*This is done in GitHub, NOT directly on the file*)

**3. Don't Allow Bypassing Items 1 and 2:**

- Next, set up a **Branch Protection Rule** that instructs GitHub not to allow any changes to the `main` / `master` branch unless it's through a Pull Request, there's no failing tests, and there's a *Code Review*.

### Branching

You can create a new branch and update your GitHub repo all from your terminal. Simply create a new branch, the swith over to it, and lastly push to GitHub. You can use the commands below.

```console
git branch new_branch
git checkout new_branch
git push -u origin new_branch
```

### Pull Requests

A pull request is when you request to merge the commits from one branch into another. For this project all of your changes should be done on another branch and NEVER directly on the `main` / `master` branch.

Look at your PowerPoint slides for guidance on how to create Pull Requests.

### Code Review

Your code must be reviewed and given feedback by a team member before it is merged into the `main` \ `master` branch. Look at your PowerPoint slides for guidance on how to *Review* and *Approve* Pull Requests.
