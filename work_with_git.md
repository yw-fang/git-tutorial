# Work with git and github

There are several ways to work with your first repository. The simplest way
should be create it onlien in your github account, and git clone it to your local computer, and revise the fies, then git add it, git commit -m 'something', and finally git push. 

One alternative simple way can be:

mkdir git-tutorial

cd git-tutorial

git init

vim README.md, and write some words in README.md.

git add README.md

git commit -m 'create README.md'

Now, go to your account, and create a new repository named 'git-tutorial', it's should be metnioned that you had better not to initialize the README file in the github website bcasuse you can later push the lcoal README.md to github.

git remote add origin git@github.com:yw-fang/git-tutorial.git

git push -u origin master

git status

#create-branch
git checkout -b work-1

git push origin work-1

#merge-branch-to-master.
git checkout master

git merge --no-ff work-1

git log --graph

#An example using git
mkdir aiida-phonopy
cd aiida-phonopy
git init 
touch README-1.md
git add READEME-1.md
git commit -m 'test'
git remote add origin git@github.com:yw-fang/aiida-phonopy.git
git push u origin master

git remote add upstream git@github.com:abelcarreras/aiida-phonopy.git
git fetch upstream

##Refrences, questions and answers

[Syncing a fork](https://help.github.com/articles/syncing-a-fork/)

[Keeping a fork up to date](https://gist.github.com/CristinaSolana/1885435)

[Git push existing repo to a new and different remote repo server](https://stackoverflow.com/questions/5181845/git-push-existing-repo-to-a-new-and-different-remote-repo-server)

[merge unrelated histories](https://stackoverflow.com/questions/40036648/git-fatal-refusing-to-merge-unrelated-histories)

[Merging an upstream repository into your fork](https://help.github.com/articles/merging-an-upstream-repository-into-your-fork/)

[Create and push a branch](https://confluence.atlassian.com/get-started-with-bitbucket/create-and-push-a-branch-862720857.html)

[Create a new branch with git and manage branches](https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches)
