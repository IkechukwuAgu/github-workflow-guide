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


