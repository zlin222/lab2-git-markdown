# git and markdown

The purpose of this lab is to get you prepared for PS1, hence the
tasks are comparable.  Here are the tasks:

## Basic git workflow

1. Ensure that you have a folder on your computer where you store
   info201 exercises.  If needed, create one.  Now use your shell to
   navigate to this directory, and write the command (or commands if
   you use multiple) here underneath.  Use markdown _code blocks_ to
   mark your commands.
   
   cd Desktop/info201/lab2
   
1. **fork** this repository on Github under your user name (see
   [course book 4.6.1](https://faculty.washington.edu/otoomet/info201-book/git-basics.html#forking-and-cloning)).

2. **clone** the forked repo to your computer (see [course
   book 4.3.3](https://faculty.washington.edu/otoomet/info201-book/git-basics.html#git-basics-getting-creating)).
   Write the command you
   used underneath in a code block.
   
3. **add a new file** "books.md" to the repo.  You can use RStudio
   (file -> new file -> markdown file), or any other tool you find
   convenient.
   
4. add a numbered list of book you like to this file
   (see [Github markdown
   docs](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)). 
   You can use
   RStudio editor, or any other editor you like.
   
5. check **git status** (see [course book
   4.4.1](https://faculty.washington.edu/otoomet/info201-book/git-basics.html#git-basics-situational-awareness)).
   Show below, in _block quote_, what does it print.

```
   Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   readme.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.Rhistory
	books.md

no changes added to commit (use "git add" and/or "git commit -a")
```
   
   Explain, in plain text, what does it mean.
   
6. **add** the new file to the repository (see [course book
  4.4.3](https://faculty.washington.edu/otoomet/info201-book/git-basics.html#git-basics-working-adding)).
  Show your command (as a
  code block).
  
```
  git add .
```

7. Was your add successful?  Check status again!  Explain what do you
   see.
   Your branch is up to date with 'origin/main'.

```
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   .Rhistory
	new file:   books.md
	modified:   readme.md
```  
   
8. Now **commit** your changes (see [course book
   4.4.4](https://faculty.washington.edu/otoomet/info201-book/git-basics.html#git-basics-working-committing)). 
   Put your command underneath in a code block.
   
```
 git commit -am "changes"
```

9. Was your commit successful?  How can you check it?  Show your
   command(s) as a code block and explain what you see!

```
git status
```
   
10. Now **push** your changes to Github (see [course book 4.4.5](https://faculty.washington.edu/otoomet/info201-book/git-basics.html#git-basics-working-pushing)).  You may
   need to create access token before you are able to push.
   
11. Go to your github page.  Can you see the books.md file there with
    all the books listed?
    
    Yes

## Folders and relative path

This task is about adding images and using relative path.

1. create a folder "images" to your repo.  You can use either `mkdir`
   command, or the file manager.

2. put an image into the folder.  It should be of a type that Github
   can render, e.g. `.jpg` or `.png`, not sure about `.heic` or other
   very new formats.  (You can just download or copy it there).
   
3. check git status.  What do you see?

   On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.DS_Store
	images/

nothing added to commit but untracked files present (use "git add" to track)

4. add image to the repo.  Show the command you are using in a code
   block.
   
```
git add .
```
   
5. check status again.  Does it indicate that the image has been
   added?
   
   Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
	new file:   .DS_Store
	new file:   images/2.jpg
   
   Yes.
   
6. what is the relative path of your image if you start walking there
   from the location of your books.md file?
   
   images/2.jpg
   
   You can check if the path is correct with something like `ls
   path-to/file`, e.g.
   ```
   ls images/picture.jpg
   ```
   it lists the file name if correct, and complains about _no suc file
   or directory_ if the path is wrong.
   
7. now add the image to your books.md file using the relative path.

8. check git status and commit

9. push

10. check on github--does your books.md file now contain the image?
   Yes. 
