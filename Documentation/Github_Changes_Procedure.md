# Github Changes Procedure

This guide describes the standard procedure for making and pushing changes to the GitHub repository using branches. It helps maintain a clean and organized workflow across collaborators.

## 1. Pull the Latest Changes from the Main Branch

Before starting any new work, ensure your local repository is up to date:

```bash
git checkout main
git pull origin main
```

## 2. Create and Switch to a New Branch

Create a new branch for your feature or fix. Use a descriptive name, such as add-model, fix-bug, or update-docs:

```bash
git checkout -b your-branch-name
```

## 3. Make Your Changes Locally

Once you're on your new branch, you can begin editing the code or documentation.

Save your changes as you work. These changes will remain local until you explicitly commit and push them.

You can check the status of your changes at any time with:

```bash
git status
```

## 4. Stage and Commit Your Changes

After making changes to files, you need to *stage* them and then *commit* them with a descriptive message.

### ✅ Stage all changes:
```bash
git add .
```

You can also stage specific files:

```bash
git add path/to/file.py
```

### ✅ Commit the staged changes:

```bash
git commit -m "Describe what you changed"
```

## 5. Push Your Branch to GitHub

Once you've committed your changes locally, push your branch to the remote GitHub repository:

```bash
git push -u main your-branch-name
```

## 6. (Optional) Open a Pull Request

After pushing your branch to GitHub, open your browser and go to the repository page. GitHub will usually show a prompt like:

> "Compare & pull request"

Click it to start a new pull request (PR).

### In the pull request:
- *Base branch* should be main (or master, depending on your repo).
- *Compare branch* should be your feature branch (e.g., add-documentation).
- Write a *clear title and description* of what your changes include.
- Optionally request reviews from collaborators.

Once approved, click *"Merge pull request"* to integrate your changes into the main branch.

> ✅ Pull requests are a best practice for collaborative projects, as they allow code review and change tracking before merging.

## 7. Switch Back to the Main Branch

After your pull request has been merged (or if you're done working on your feature branch), switch back to the main branch locally:

```bash
git checkout main
```

## 8. Pull the Latest Main Again

After switching back to the main branch, make sure it’s fully up to date with the latest changes from GitHub (including your recently merged pull request):

```bash
git pull origin main
```
