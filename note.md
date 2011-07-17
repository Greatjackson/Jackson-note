ktop:~$ sudo su
[sudo] password for akaedu:
root@akaedu-desktop:/home/akaedu# whoami
root
root@akaedu-desktop:/home/akaedu# exit
exit
akaedu@akaedu-desktop:~$ whoami
akaedu
akaedu@akaedu-desktop:~$

akaedu@akaedu-desktop:~/lgnote$ chmod 666 note
akaedu@akaedu-desktop:~/lgnote$ ls -l note
-rw-rw-rw- 1 akaedu akaedu 208 2011-07-16 11:20 note
akaedu@akaedu-desktop:~/lgnote$

akaedu@akaedu-desktop:~/lgnote$ chmod a+x note
akaedu@akaedu-desktop:~/lgnote$ ls -l note
-rwxrwxrwx 1 akaedu akaedu 385 2011-07-16 11:33 note
akaedu@akaedu-desktop:~/lgnote$

统一删除含有写保护的目录   -rf

akaedu@akaedu-desktop:~$ ls
aaa    ccc      dir        Downloads         h.c         index.html.1  Music     psjicfh  Templates  Videos  下载
a.out  Desktop  Documents  examples.desktop  index.html  lgnote        Pictures  Public   tg-note    图片    桌面
akaedu@akaedu-desktop:~$ vim h.c
akaedu@akaedu-desktop:~$ cp h.c h1.c
akaedu@akaedu-desktop:~$ vim h1.c
akaedu@akaedu-desktop:~$ diff h.c h1.c
5a6
>       printf("hello\n");
akaedu@akaedu-desktop:~$ diff -u h.c h1.c >h.diff
akaedu@akaedu-desktop:~$ vim h.
h.c     h.diff
akaedu@akaedu-desktop:~$ vim h.diff
akaedu@akaedu-desktop:~$ ls
aaa    ccc      dir        Downloads         h1.c  h.diff      index.html.1  Music     psjicfh  Templates  Videos  下载
a.out  Desktop  Documents  examples.desktop  h.c   index.html  lgnote        Pictures  Public   tg-note    图片    桌面

akaedu@akaedu-desktop:~$ ls
aaa    ccc      dir        Downloads         h1.c  h.diff      index.html.1  Music     psjicfh  Templates  Videos  下载
a.out  Desktop  Documents  examples.desktop  h.c   index.html  lgnote        Pictures  Public   tg-note    图片    桌面
akaedu@akaedu-desktop:~$ patch h.c < h.diff
patching file h.c
akaedu@akaedu-desktop:~$ vim h.c
akaedu@akaedu-desktop:~$ diff h.c h1.c
akaedu@akaedu-desktop:~$

akaedu@akaedu-desktop:~/lgnote$ cd
akaedu@akaedu-desktop:~$ patch -R h.c < h.diff
patching file h.c
akaedu@akaedu-desktop:~$ vim h.c
akaedu@akaedu-desktop:~$

akaedu@akaedu-desktop:~/lgnote$ ls -a
.  ..  note  qq
akaedu@akaedu-desktop:~/lgnote$

akaedu@akaedu-desktop:~$ git add h.c
akaedu@akaedu-desktop:~$ git commit -a -m "first version "     "-a all"   "-m message "
[master (root-commit) 3b3e81d] first version
 Committer: akaedu <akaedu@akaedu-desktop.(none)>
Your name and email address were configured automatically based
on your username and hostname. Please check that they are accurate.
You can suppress this message by setting them explicitly:

    git config --global user.name "Your Name"
    git config --global user.email you@example.com

If the identity used for this commit is wrong, you can fix it with:

    git commit --amend --author='Your Name <you@example.com>'

 1 files changed, 6 insertions(+), 0 deletions(-)
 create mode 100644 h.c
akaedu@akaedu-desktop:~$ tig
akaedu@akaedu-desktop:~$ history 10
  774  vim note
  775  ls -a
  776  vim note
  777  cd
  778  git init
  779  fg 1
  780  git add h.c
  781  git commit -a -m "first version "
  782  tig
  783  history 10
akaedu@akaedu-desktop:~$

#网络git:
Global setup:

 Set up git
  git config --global user.name "Your Name"
  git config --global user.email 308584349@163.com


Next steps:

  mkdir Jackson-note
  cd Jackson-note
  git init
  touch README
  git add README
  git commit -m 'first commit'
  git remote add origin git@github.com:Greatjackson/Jackson-note.git
  git push -u origin master
      

Existing Git Repo?

  cd existing_git_repo
  git remote add origin git@github.com:Greatjackson/Jackson-note.git
  git push -u origin master
      

Importing a Subversion Repo?

  Click here
      

When you're done:

  Continue

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

if you want insert ang substance,you must enter insert mode,or the computer will search the first letter "i",and insert aftercontent.

how to delete indent  mv -rf .vimrc
