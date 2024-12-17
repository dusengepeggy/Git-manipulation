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

## Exercise 2

### **Steps**

### 1. Work on the `ft/service-redesign` branch
1. **Checkout the `main` branch and pull the latest changes**:
   ```bash
   git checkout main
   git pull origin main
   ```

2. **Create a new branch named `ft/service-redesign`**:
   ```bash
   git checkout -b ft/service-redesign
   ```

3. **Make changes to the `service.html` page**:
   - Modify the file and save changes.
   - Stage and commit the changes:
     ```bash
     git add service.html
     git commit -m "Service page redesign changes"
     ```

4. **Push the changes to GitHub**:
   ```bash
   git push -u origin ft/service-redesign
   ```

5. **Create a Pull Request (PR)**:
   - Open a new PR for the `ft/service-redesign` branch targeting the `main` branch.

---

### **2. Add conflicting changes to the `main` branch**
1. **Checkout the `main` branch**:
   ```bash
   git checkout main
   ```

2. **Make new changes to the `service.html` file**:
   - Modify the same part of the file that you changed in the `ft/service-redesign` branch. 
   - Save, stage, and commit the changes:
     ```bash
     git add service.html
     git commit -m "Conflicting changes to service.html on main branch"
     ```

3. **Push the changes to GitHub**:
   ```bash
   git push origin main
   ```

---

### **3. Observe conflicts in the GitHub PR**
- Go to the Pull Request you created for the `ft/service-redesign` branch.
- You will now see that there are **merge conflicts** between the `ft/service-redesign` branch and the `main` branch.

---

### **4. Resolve the conflicts locally**
1. **Checkout the `ft/service-redesign` branch**:
   ```bash
   git checkout ft/service-redesign
   ```

2. **Compare the `ft/service-redesign` branch with the `main` branch using `git diff`**:
   ```bash
   git diff main
   ```

   - This command shows the differences between the two branches.

3. **Merge the `main` branch into `ft/service-redesign`**:
   ```bash
   git merge main
   ```

   - You will see **merge conflicts** in the `service.html` file.

4. **Resolve the conflicts**:
   - Open the conflicted file (e.g., `service.html`) in your code editor.
   - Look for the conflict markers:
     ```html
     <<<<<<< HEAD
     Changes from ft/service-redesign branch
     =======
     Changes from main branch
     >>>>>>> main
     ```
   - Edit the file to keep the desired changes and remove the conflict markers.

5. **Stage the resolved file**:
   ```bash
   git add service.html
   ```

6. **Commit the merge**:
   ```bash
   git commit -m "Resolved conflicts between main and ft/service-redesign"
   ```

7. **Push the changes to GitHub**:
   ```bash
   git push origin ft/service-redesign
   ```

---

# **Bundle 3**

## **Exercise 1**

### **Steps**

1. **Create a new branch `ft/team-page`**:
   ```bash
   git checkout -b ft/team-page
   ```

2. **Create a new HTML page named `team.html` and add some changes**:
   - Add content to the `team.html` file.
   - Stage and commit the changes:
     ```bash
     git add team.html
     git commit -m "Add team.html page"
     ```

3. **Push the changes and create a Pull Request (PR)**:
   ```bash
   git push origin ft/team-page
   ```
   - Open a PR for the `ft/team-page` branch.

4. **Go back to the `main` branch**:
   ```bash
   git checkout main
   ```

5. **Create a new branch `ft/contact-page`**:
   ```bash
   git checkout -b ft/contact-page
   ```

6. **Cherry-pick the last commit from the `ft/team-page` branch**:
   - Switch back to the `ft/team-page` branch and copy the commit hash using `git log`:
     ```bash
     git checkout ft/team-page
     git log
     ```
   - Copy the hash of the last commit.

   - Switch back to `ft/contact-page` and cherry-pick the commit:
     ```bash
     git checkout ft/contact-page
     git cherry-pick <commit-hash>
     ```

7. **Add changes for the contact page, commit, and push**:
   - Modify the `contact.html` file or add content:
     ```bash
     git add contact.html
     git commit -m "Add contact page content"
     git push origin ft/contact-page
     ```
   - Open a PR for the `ft/contact-page` branch.

8. **Create a new branch `ft/faq-page` from `ft/contact-page`**:
   ```bash
   git checkout -b ft/faq-page
   ```

9. **Create a new `faq.html` page and add changes**:
   - Add content to the `faq.html` file.
   - Stage, commit, and push the changes:
     ```bash
     git add faq.html
     git commit -m "Add FAQ page"
     git push origin ft/faq-page
     ```

10. **Revert the last commit on `ft/team-page`**:
    - Use the commit hash you copied earlier:
      ```bash
      git checkout ft/team-page
      git revert <commit-hash>
      ```
    - Push the reverted changes and open a new PR:
      ```bash
      git push origin ft/team-page
      ```

---

## **Exercise 2**

### **Steps**

1. **Create a new branch `ft/home-page-redesign` from `ft/faq-page`**:
   ```bash
   git checkout -b ft/home-page-redesign
   ```

2. **Go back to the `main` branch and make changes**:
   - Switch to the `main` branch:
     ```bash
     git checkout main
     ```
   - Add changes to files, stage, commit, and push:
     ```bash
     git add .
     git commit -m "Update main branch with new changes"
     git push origin main
     ```

3. **Rebase `ft/home-page-redesign` onto the updated `main` branch**:
   ```bash
   git checkout ft/home-page-redesign
   git rebase main
   ```
   - If conflicts occur, resolve them manually:
     ```bash
     git add <resolved-files>
     git rebase --continue
     ```

4. **Add changes to the home page and commit**:
   - Modify the `home.html` file:
     ```bash
     git add home.html
     git commit -m "Redesign home page"
     ```

5. **Push the rebased branch**:
   ```bash
   git push origin ft/home-page-redesign
   ```

6. **Create a PR for the changes**:
   - Open a Pull Request targeting the `main` branch.

---
# **Bundle 4**

## **Exercise 1**

### **Steps**

1. **Checkout the `main` branch**:
   ```bash
   git checkout main
   ```

2. **Create a new repository on GitHub**:
   - Go to GitHub and create a new repository.

3. **Add the new repository as a second remote**:
   - Copy the repository URL.
   - Add it as a second remote named `git-copy`:
     ```bash
     git remote add git-copy <repo-url>
     ```

4. **Make changes to the home page**:
   - Edit the file (e.g., `home.html`) and save the changes.

5. **Commit the changes**:
   ```bash
   git add home.html
   git commit -m "Update home page with new changes"
   ```

6. **Push changes to both remotes**:
   - Push to `origin`:
     ```bash
     git push origin main
     ```
   - Push to `git-copy`:
     ```bash
     git push git-copy main
     ```

---

## **Exercise 2**

### **Steps**

1. **Checkedout a new branch named `ft/footer`**:
   ```bash
   git checkout -b ft/footer
   ```

2. **Made and committed the changes**:
   - Add some changes to the branch:
     ```bash
     git add .
     git commit -m "Add initial footer changes"
     ```
   - Add more changes and commit again:
     ```bash
     git add .
     git commit -m "Add additional footer updates"
     ```

3. **Pushed changes and created a PR**:
   ```bash
   git push origin ft/footer
   ```
   - Go to GitHub and create a Pull Request (PR) for the `ft/footer` branch.

4. **Checkedout the `main` branch**:
   ```bash
   git checkout main
   ```

5. **Created a new branch named `ft/squashing`**:
   ```bash
   git checkout -b ft/squashing
   ```

6. **Squashed the changes from the `ft/footer` branch**:
   - Merged the `ft/footer` branch with squash:
     ```bash
     git merge --squash ft/footer
     ```
   - Committed the squashed changes with a new message:
     ```bash
     git commit -m "footer changes squashing"
     ```

7. **Pushed the changes and create a PR**:
   ```bash
   git push origin ft/squashing
   ```
   - Go to GitHub and create a PR for the `ft/squashing` branch.

---




     
