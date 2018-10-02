Woking for a fork will not be displayed in the contribution dashboard
until those commints have been merged into the upstream.
If you don't plan to merge the changes upstream, you can consider working in a standalong repository instead working for a fork.

Here are the steps:

1. Clone the repository (use git clone) you want to use.

2. Create a new repository on GitHub webpage.

3. [Change the local repository's remote URL](https://help.github.com/articles/changing-a-remote-s-url/) to point to your new repository.

4. [Push the local repository to your new repository on GitHub](https://help.github.com/articles/pushing-to-a-remote/).

If you have erros when using git push, probably you also need rebase 
your local repository: 1) git rebase origin/master; 2) git pull --rebase; 3) git push
