# Repository for DST 490
**Semester: Fall 2026**

- Files are organized by the day that they occur in the [course calendar](https://docs.google.com/document/d/1gkt2Nr6lZZy2YuTlNgBIMmQU8GYxrItWnLIzjUeiTg0/edit?tab=t.0#bookmark=id.v39ch8ejcl7j).

- **To make a fork the repo**, use the following command in the RStudio console (one time only):

```r
usethis::create_from_github(
  "https://github.com/AugsburgDST490/2026SEM1_Files.git",
  fork = TRUE,
  destdir = "YOUR_LOCATION") # <-- your location on the computer goes here
```

What this does is:

- Makes a fork of the classroom files repo onto your github.
- Clones the copy of the repository to your local computer.
- Configures your repository to pull and push **onto your repository only**
- Allows you to track my classroom repository for changes.

- **Next: set pushes to your github repo (not mine, the one you forked):**, use the following command in the terminal (one time only):
```
git push -u origin main

```

- **To check** use the following command in the terminal:
```
git remote -v  # You should see `origin` (your fork) and `upstream` (the class repo).
```

- **To update your fork with any changes:** Do this before beginning new work and whenever they want any updates. **Save all local files.**  Then run the following:

```
# Stage files:
git add file1.qmd file2.qmd # list all files

# Alternatively you can do:
# git add .   # optional method

Commit:
git commit -m "Add data cleaning script"

Send:
git push origin main

# Check to see if there is upstream work:
git fetch upstream

# See a list of incoming commits that exist on upstream but not locally
git log HEAD..upstream/main --oneline

# Pull the work in:
git pull upstream main

git stash  # This safely stores staged / unstaged changes
```

- **Merge conflicts:** You *may* get a merge conflict in the rebase if I've updated a file that you are working on. You will need to edit them accordingly:

```
<<<<<<< Updated upstream
(instructor code)
=======
(your stashed edits)
>>>>>>> Stashed changes
```

Then once you've made the changes:

```
git add <file>
git rebase --continue   # only needed if rebase was still in progress
```





