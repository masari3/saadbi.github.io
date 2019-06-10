$ cd ~/Dropbox/Git
$ git init --bare mytestrepo.git
  Initialized empty Git repository in /Users/jetheis/Dropbox/Git/mytestrepo.git/

$ cd ~
$ mkdir testrepo
$ cd testrepo
$ git init
  Initialized empty Git repository in /Users/jetheis/testrepo/.git/
$ echo "Some Text" > testfile.txt
$ git add testfile.txt
$ git commit -m "Add a test file"
  [master (root-commit) 0220f05] Add a test file
   1 file changed, 1 insertion(+)
   create mode 100644 testfile.txt
$ echo "More text" >> testfile.txt
$ git commit testfile.txt -m "Add more text"
  [master f014b59] Add more text
   1 file changed, 1 insertion(+)

$ cat testfile.txt
  Some Text
  More text
$ git log
  commit f014b59d8d3af6e20bd5d671bd98f86e26fba743
  Author: Jimmy Theis
  Date:   Sun Feb 17 12:10:19 2013 -0500

      Add more text

  commit 0220f050e087d92ad96a549c2b913363f551b7fc
  Author: Jimmy Theis
  Date:   Sun Feb 17 12:08:50 2013 -0500

      Add a test file


$ git remote add origin ~/Dropbox/Git/mytestrepo.git

$ git push -u origin master
  Counting objects: 6, done.
  Delta compression using up to 4 threads.
  Compressing objects: 100% (2/2), done.
  Writing objects: 100% (6/6), 458 bytes, done.
  Total 6 (delta 0), reused 0 (delta 0)
  Unpacking objects: 100% (6/6), done.
  To /Users/jetheis/Dropbox/Git/mytestrepo.git
   * [new branch]      master -> master
  Branch master set up to track remote branch master from origin.
