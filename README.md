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
     
