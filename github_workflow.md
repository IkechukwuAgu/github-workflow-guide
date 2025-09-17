# 📝 Step-by-Step GitHub Workflow Practice

## 1. Set Up Your Project  

* Make a folder on your computer:  

```bash
mkdir my-first-github-project
cd my-first-github-project
```


* Initialize Git:  

```bash
git init
```
* create a file
  
```bash
echo "# My First GitHub Project" > README.md
```

## 2. First Commit

* Stage your file:
  

```bash
git add README.md

```
* Commit it:
```bash
git commit -m "Add: initial README"
```

## 3. Push to GitHub

* Create a new empty repo on GitHub.

* Connect your local project:

```bash 
git remote add origin https://github.com/<your-username>/my-first-github-project.git
```

```bash
git push -u origin main
```

GitHub Branching Workflow
-------------------------------

### 🔀 What is a Branching Workflow?

A branching workflow is a strategy for how you use branches in Git to manage your project’s code.
Instead of committing everything directly to the `main` branch, you create separate branches for features, fixes, or experiments.

This makes collaboration easier and prevents breaking the main code.


 🛠 Common GitHub Branching Workflow
-------------------------------

Here’s the step-by-step:

#### 1. Main Branch ( `main` or `master`)

  * This is the production-ready code.

  * Nothing should be committed directly here (except hotfixes).

  * Always stable.

#### 2. Feature Branches

  * For new features, create a branch from main.

  * Example:
  
  ``` bash 
  git checkout -b feature/login-system
  ```
  * Work on your feature inside this branch.

  * Commit changes regularly.


#### 3. Commit and Push

* Stage and commit your work:
```bash
git add .
git commit -m "Add login page UI"
```


* Push to GitHub:

``` bash 
git push origin feature/login-system
```


#### 4. Pull Request (PR)

* On GitHub, open a Pull Request from your branch → main.

* Team members review your code.

* If approved, merge it.

#### 5. Merging

* Merge your branch into main after review.

* Delete the feature branch to keep repo clean.

#### 6. Hotfix Branch

* If there’s a bug in production:

```bash
git checkout -b hotfix/bug-fix
```
* Fix it, then merge quickly into main.


#### 🔑 Branch Naming Convention

* main → stable production code

* feature/* → new features

* bugfix/* → bug fixes

* hotfix/* → urgent fixes

