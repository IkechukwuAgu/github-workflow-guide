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
---

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

---



#### 📌 Example Workflow in Action 

1. Clone repo:

```bash
git clone git@github.com:username/project.git
cd project
```


2. Create branch for feature:

```bash 
git checkout -b feature/user-profile
```


3. Work, commit, and push:

```bash 
git push origin feature/user-profile 
```


4. Open PR → Review → Merge → Delete branch.

<p align="center">
<img src="./img/ChatGPT Image Sep 16, 2025, 10_28_31 PM.png" alt="My Logo" width="200">
</p>


--- 

🔥 What is a Merge Conflict?
---

A merge conflict happens when Git can’t automatically combine changes from two branches because the same part of the code was changed differently in each branch.
Git doesn’t know which version to keep — so it asks you to resolve it manually.

#### ⚠️ Example Scenario

1. You and your teammate both branch off main.

*  You change line 10 of index.html.

*  Your teammate also changes line 10.

2. When you try to merge, Git says:

```bash
 CONFLICT (content): Merge conflict in index.html 
 ```

#### 🛠 How to Fix a Merge Conflict

1. See which files have conflicts

```bash
 git status 
```

##### 1. Open the conflicted file

You’ll see markers like this:

```html
<<<<<<< HEAD
<p>Hello from my branch</p>
=======
<p>Hello from teammate's branch</p>
>>>>>>> feature/teammate

```
* <<<<<<< HEAD → your code (current branch)

* ======= → divider  

*  >>>>>>> → code from the branch you are merging in

##### 3. Resolve the conflict

Decide what to keep:

```html 
<p>Hello from both branches</p> 
```


 ##### 4. Mark conflict as resolved
git add index.html

##### 5. Complete the merge

```bash 
git commit
```


Now the merge is successful 🚀.

---
🔑 Tips

* Communicate with teammates — agree on which changes to keep.

* Use tools like VS Code, GitHub Desktop, or GitHub’s web editor to resolve conflicts more easily.

* Keep commits small and frequent to reduce conflict chances.

---

