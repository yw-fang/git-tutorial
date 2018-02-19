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

git remote upstream git@github.com:abelcarreras/aiida-phonopy.git
git fetch upstream
