ktop:~$ sudo su

[sudo] password for akaedu:

root@akaedu-desktop:/home/akaedu# whoami

root

root@akaedu-desktop:/home/akaedu# exit

exit

akaedu@akaedu-desktop:~$ whoami

akaedu

akaedu@akaedu-desktop:~$

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

akaedu@akaedu-desktop:~/lgnote$ chmod 666 note

akaedu@akaedu-desktop:~/lgnote$ ls -l note

-rw-rw-rw- 1 akaedu akaedu 208 2011-07-16 11:20 note

akaedu@akaedu-desktop:~/lgnote$

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

akaedu@akaedu-desktop:~/lgnote$ chmod a+x note

akaedu@akaedu-desktop:~/lgnote$ ls -l note

-rwxrwxrwx 1 akaedu akaedu 385 2011-07-16 11:33 note

akaedu@akaedu-desktop:~/lgnote$

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

统一删除含有写保护的目录   -rf

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

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

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

akaedu@akaedu-desktop:~$ ls

aaa    ccc      dir        Downloads         h1.c  h.diff      index.html.1  Music     psjicfh  Templates  Videos  下载
a.out  Desktop  Documents  examples.desktop  h.c   index.html  lgnote        Pictures  Public   tg-note    图片    桌面

akaedu@akaedu-desktop:~$ patch h.c < h.diff

patching file h.c

akaedu@akaedu-desktop:~$ vim h.c

akaedu@akaedu-desktop:~$ diff h.c h1.c

akaedu@akaedu-desktop:~$

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

akaedu@akaedu-desktop:~/lgnote$ cd

akaedu@akaedu-desktop:~$ patch -R h.c < h.diff

patching file h.c

akaedu@akaedu-desktop:~$ vim h.c

akaedu@akaedu-desktop:~$

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

akaedu@akaedu-desktop:~/lgnote$ ls -a

.  ..  note  qq

akaedu@akaedu-desktop:~/lgnote$

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

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

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

网络git:

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
i  git remote add origin git@github.com:Greatjackson/Jackson-note.git
  git push -u origin master
      

Importing a Subversion Repo?

  Click here
      
When you are done:

Continue

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

if you want insert ang substance,you must enter insert mode,or the computer will search the first letter "i",and insert after

content.

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

how to delete indent 

	 mv -rf .vimrc

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

akaedu@akaedu-desktop:~/lgnote$ ls

note.md

akaedu@akaedu-desktop:~/lgnote$ git init 

Initialized empty Git repository in /home/akaedu/lgnote/.git/

akaedu@akaedu-desktop:~/lgnote$ ls -a 

.  ..  .git  note.md

akaedu@akaedu-desktop:~/lgnote$ git add note.md

akaedu@akaedu-desktop:~/lgnote$ git commit -a -m "first "

[master (root-commit) 8cee81f] first

 1 files changed, 130 insertions(+), 0 deletions(-)
 create mode 100644 note.md

akaedu@akaedu-desktop:~/lgnote$ tig 

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

akaedu@akaedu-desktop:~/aaa$ gcc -Wall lg.c

akaedu@akaedu-desktop:~/aaa$ echo $?

0

akaedu@akaedu-desktop:~/aaa$ ./a.out

hello!

akaedu@akaedu-desktop:~/aaa$ 

akaedu@akaedu-desktop:~/aaa$ gcc -Wall lg.c  "show the error and warning of  compile programme "

akaedu@akaedu-desktop:~/aaa$ echo $?        "show the return value of the main function "

0

akaedu@akaedu-desktop:~/aaa$ ./a.out

hello!

akaedu@akaedu-desktop:~/aaa$ 

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

:sh     "creat a new bush in vim"

ctrl+d or exit   "exit the new bush "

u       "undo but in new bush mode"

ctrl+r   "redo in undo mode"

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa

akaedu@akaedu-desktop:~/lgnote$ ls

akaedu@akaedu-desktop:~/lgnote$ ls

akaedu@akaedu-desktop:~/lgnote$ la

.git

akaedu@akaedu-desktop:~/lgnote$ git throw

HEAD is now at 372ec83 f

akaedu@akaedu-desktop:~/lgnote$ ls

note.md

akaedu@akaedu-desktop:~/lgnote$ vim note.md 

akaedu@akaedu-desktop:~/lgnote$ 

aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa


akaedu@akaedu-desktop:~$ wget http://media.happypeter.org/happycasts/happycity/taiyuan_gongye-casts/git-hello-world.ogv

--2011-07-20 17:02:50--  http://media.happypeter.org/happycasts/happycity/taiyuan_gongye-casts/git-hello-world.ogv

Resolving media.happypeter.org... 122.115.61.189

Connecting to media.happypeter.org|122.115.61.189|:80... connected.

HTTP request sent, awaiting response... 200 OK

Length: 17619395 (17M) [video/ogg]

Saving to: `git-hello-world.ogv'


100%[===================================================================================>] 17,619,395   125K/s   in 3m 2s   

2011-07-20 17:05:52 (94.6 KB/s) - `git-hello-world.ogv' saved [17619395/17619395]

akaedu@akaedu-desktop:~$ ls

aaa       bookmarks.html  Documents              git-hello-world.ogv  index.html    Music     Templates  下载

aaa.html  ccc             Downloads              h1.c                 index.html.1  Pictures  tg-note    桌面

aaa.md    Desktop         examples.desktop       h.c                  lgnote        psjicfh   Videos

a.out     dir             Firefox_wallpaper.png  h.diff               lg-project    Public    图片

akaedu@akaedu-desktop:~$ totem git-hello-world.ogv                   "when you can not find a file under directory or mistake to delete it,perhaps you feel anxious,but I will say do not worry,you only do that input 'git throw',all is ok,because the missed file is hiding  saved in '.git'   " 
