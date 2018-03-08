Here, I show how to ecrypt files in GitHub.

(This file is exactly same to encrypt-file-in-GitHub.md, but unencrypt-file-in-GitHub.md is unencrypted and the contents can be displayed in GitHub.)

In the begining, I tried to use git-crypt, but I found gpg key generation does not
work in my current mac osx system. Other guys also mentioned this unsolved problemsin the internet. Hence, I switched to use transcrypt

I show you how to use transcrpt in MacOS:

$ brew install transcrypt
$ cd git-tutorial/
$ transcrypt
Encrypt using which cipher? [aes-256-cbc]
Generate a random password? [Y/n]
unable to write 'random state'

*.mmd filter=crypt diff=crypt
Repository metadata:

  GIT_WORK_TREE:  /Users/ywfang/FANG/git/git-tutorial
  GIT_DIR:        /Users/ywfang/FANG/git/git-tutorial/.git
  GIT_ATTRIBUTES: /Users/ywfang/FANG/git/git-tutorial/.gitattributes

The following configuration will be saved:

  CIPHER:   aes-256-cbc
  PASSWORD: 1cp02JPVSxqeDpxgTyH2WD9y9KQw0uK1K3I6JsGL

Does this look correct? [Y/n]

The repository has been successfully configured by transcrypt.

$ echo 'crypt-files-in-GitHub.md  filter=crypt diff=crypt' > .gitattributes

$ git add .gitattributes crypt-files-in-GitHub.md

$ git commit -m 'add an encrypted version for crypt-files-in-GitHub.md'

$ git push

When you clone my repository in your computer, you can find
the file crypt-files-in-GitHub.md is encrpted. 

This is the information that should be used to 'unlock' the file:

h44:git-tutorial ywfang$ transcrypt --display
The current repository was configured using transcrypt version 1.0.3
and has the following configuration:

  GIT_WORK_TREE:  /Users/ywfang/FANG/git/git-tutorial
  GIT_DIR:        /Users/ywfang/FANG/git/git-tutorial/.git
  GIT_ATTRIBUTES: /Users/ywfang/FANG/git/git-tutorial/.gitattributes

  CIPHER:   aes-256-cbc
  PASSWORD: 1cp02JPVSxqeDpxgTyH2WD9y9KQw0uK1K3I6JsGL

 filter=crypt diff=crypt
Copy and paste the following command to initialize a cloned repository:

  transcrypt -c aes-256-cbc -p '1cp02JPVSxqeDpxgTyH2WD9y9KQw0uK1K3I6JsGL'
