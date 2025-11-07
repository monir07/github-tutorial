To change the remote URL in Git, follow these steps:
Navigate to your local repository: Open your terminal or command prompt and use the cd command to go into your local Git repository's directory.
কোড

    cd /path/to/your/repository
View current remote URLs (optional but recommended): Before making changes, you can see the existing remote URLs associated with your repository using the git remote -v command. This will show you the fetch and push URLs for each remote.
কোড

    git remote -v
You will likely see output similar to this:
কোড

    origin  https://github.com/user/old-repo.git (fetch)
    origin  https://github.com/user/old-repo.git (push)
Change the remote URL: Use the git remote set-url command, specifying the remote name (commonly "origin") and the new URL. 
কোড

    git remote set-url origin <new_url>
