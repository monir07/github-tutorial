Removing all commits in Git to effectively reset your repository to an initial state without any commit history can be achieved by creating a new, "orphan" branch. This process essentially discards the entire commit history while preserving the current working directory's files.
Here are the steps to remove all commit history:
Create an orphan branch: This creates a new branch with no parent commits, effectively starting a new history.
কোড

    git checkout --orphan new-root
Add all files to the staging area: This stages all the files in your current working directory for the initial commit on the new branch.
কোড

    git add -A
Commit the current state: This creates the first commit on your new orphan branch, representing the current state of your files as the initial commit.
কোড

    git commit -m "Initial commit"
Delete the old main branch: This removes the branch that contained the old commit history.
কোড

    git branch -D main
(Replace main with the name of your old branch if it's different, e.g., master.)
Rename the new branch to main: This renames your new orphan branch to main, making it the primary branch of your repository.
কোড

    git branch -m main
(Again, replace main with your desired primary branch name if needed.)
Force push to your remote repository: This step is crucial if you want to update your remote repository (e.g., GitHub, GitLab) with the new, clean history. Use this with extreme caution, especially in shared repositories, as it overwrites the remote history and can cause problems for collaborators.
কোড

    git push -f origin main
(Replace main and origin if your branch or remote names are different.)
