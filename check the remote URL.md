To check the remote URL in Git, navigate to your local Git repository in your terminal or command prompt and use one of the following commands:
To list all configured remotes and their associated URLs:
কোড

    git remote -v
This command displays both the fetch and push URLs for each remote configured in your repository. The -v flag stands for "verbose" and provides the URLs along with the remote names. 
To get the URL of a specific remote (e.g., origin):
কোড

    git config --get remote.origin.url
This command retrieves and displays only the URL for the specified remote (in this case, origin). Replace origin with the name of your remote if it's different.
To view more detailed information about a specific remote:
কোড

    git remote show origin
This command provides comprehensive information about the origin remote, including its fetch and push URLs, tracked branches, and more. Replace origin with the name of your remote if needed.
