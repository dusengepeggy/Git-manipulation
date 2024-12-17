# **Bundle 1**

## Exercise 1

1. **Create a project folder & initialize Git:**
   - Create a new folder for your project.
   - Initialize a Git repository:
     ```bash
     git init
     ```

2. **Make changes to the project:**
   - Add new files and their contents to the folder.

3. **Rename your main branch:**
   - Rename `master` to `main` (or vice versa):
     ```bash
     git branch -m main
     ```
     If your branch is already `main`, rename it to `master` and back to `main`:
     ```bash
     git branch -m master
     git branch -m main
     ```

4. **Stage and commit your changes:**
   - Stage all changes:
     ```bash
     git add .
     ```
   - Commit the changes:
     ```bash
     git commit -m "Initial commit"
     ```

5. **Create a GitHub repository and connect it with your project:**
   - On GitHub, create a new repository.
   - Add the remote URL to your local project:
     ```bash
     git remote add origin <your-repo-url>
     ```

6. **Push your changes to GitHub:**
   - Push the changes:
     ```bash
     git push -u origin main
     ```

7. **Create a new branch `dev`:**
   - Create and switch to the `dev` branch:
     ```bash
     git checkout -b dev
     ```

8. **Create another branch `test` from `dev`:**
   - From the `dev` branch:
     ```bash
     git checkout -b test
     ```

9. **Delete the `test` branch from the `dev` branch:**
   - Switch back to the `dev` branch:
     ```bash
     git checkout dev
     ```
   - Delete the `test` branch:
     ```bash
     git branch -d test
     ```

---

## Exercise 2

1. **Create a `home.html` file:**
   - Add HTML changes to the file and save it.
   - Stash your changes:
     ```bash
     git stash push -m "home.html changes"
     ```

2. **Create an `about.html` file:**
   - Add HTML changes to the file and save it.
   - Stash your changes:
     ```bash
     git stash push -m "about.html changes"
     ```

3. **Create a `team.html` file:**
   - Add HTML changes to the file and save it.
   - Stash your changes:
     ```bash
     git stash push -m "team.html changes"
     ```

4. **Restore the `about.html` changes:**
   - Use `stash pop`:
     ```bash
     git stash pop "stash@{1}"
     ```

5. **Restore the `home.html` changes:**
   - Use `stash pop` with an index:
     ```bash
     git stash pop "stash@{1}"
     ```

6. **Commit and push your changes:**
   - Stage and commit the current changes:
     ```bash
     git add .
     git commit -m "Add home and about pages"
     ```
   - Push the changes to GitHub:
     ```bash
     git push
     ```

7. **Restore the `team.html` changes:**
   - Use `stash pop` with an index:
     ```bash
     git stash pop 
     ```

8. **Reset the current changes:**
   - Discard changes in `team.html` and revert to the last commit:
     ```bash
     git reset team.html
     git checkout -- team.html
     ```
# **Bundle 2**

## Exercise 1

1. **Created a new branch named `ft/bundle-2`:**
   - Create and switch to the branch:
     ```bash
     git checkout -b ft/bundle-2
     ```

2. **Added new changes to thr project:**
   - Create a new file `services.html` and add some content to it.

3. **Committed the changes:**
   - Stage and commit the changes:
     ```bash
     git add services.html
     git commit -m "Add services.html page"
     ```

4. **Created a Pull Request:**
   - Push the branch to GitHub:
     ```bash
     git push -u origin ft/bundle-2
     ```
   - On GitHub, opened a Pull Request against the `main` branch.

5. **Request a Review and Merge the Pull Request:**
   - Assigned a reviewer to the Pull Request and request a review.

 
     
