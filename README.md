# intro
Welcome!

In this guide, we will be teaching you how to use `git`, a sharing tool for code. This is a fundamental tool for sharing and collaborating with people, so let's get this right!

### What's Git?
`git` is a tool for sharing collections of files which change over time.

If you want to deep dive into what git is, read this: [TODO](todo).

### Git vs Github
`git` is a tool for sharing collections of files. `github` is a centralised space to store collections of files, accessible using `git`. 

If you like metaphors, `github` is to `git` as `outlook` is to `email`.

## 1 Installing Git
Your `git` journey will be different depending on what platform you're using. Select from the below:
### Windows
1. If you're on windows, you'll need to start by downloading git. Go here: <https://git-scm.com/downloads>
2. Once you get to the screen where there are a whole bunch of checkboxes, leave it at the default configuration. [TODO: ADD IMAGE]
3. When you get to the screen where it says 'Use VIM as the editor by default, **change it to Nano**. Unless you're a masochist.
4. Choose 'Use windows' default console window' when you get to it.
5. Leave the rest of the config as is.
### MacOSX
1. If you're on MacOSX, you'll need to start by installing Homebrew, which then can install git, so copy this command: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
2. Open up Terminal, which can be found through Spotlight, paste the link and then press enter. (You might need to enter your computer password)
3. Next press enter when prompted, and let the terminal install Homebrew. You'll know this is over when you stop getting prompts.
4. Type `brew install git` into terminal and press enter, this is installing Git. Just let the computer do its thing and you're done.
### Linux
1. Follow the instructions here: <https://git-scm.com/downloads>
2. If you're using Linux, I'm assuming you know what the terminal, `apt`, and `sudo` are. If not, well, ask me.

### WARNING
Once you've installed `git`, you'll need to CLOSE AND REOPEN ALL PREVIOUSLY OPEN TERMINAL WINDOWS, as older terminal windows will not recognise `git` as a command.

## 2 Using the terminal
1. Open a terminal window.
   - Windows: Type in 'cmd' into your start. If all goes well, a black cmd window should appear.
   - Linux: Type in 'terminal' into your start. If all goes well, a black terminal window should appear.
   - OSX: Type in 'terminal' into your launcher. If all goes well, a white terminal window should appear.
2. [Mac Only] Type in `pwd`. This stands for "Print Working Directory", and will tell you where your terminal is currently working in.
   - If you're on Windows, cmd should constantly show you where you are via the path in front of the arrow.
3. Open a normal file explorer, so you can see what's going on.
   - Windows: Type `explorer .`
   - OSX: Type `open .`
   - Linux: Type `nautilus .`
3. Type in `mkdir USRC_TEST`. This will make a new folder called USRC_TEST. Verify in your file explorer that there is a new folder there.
4. Type in `cd USRC_TEST`. This will move your terminal window to work in your new folder.
   - OSX, Linux: Type `pwd` again and verify that the directory has changed.
   - Windows: Check that your cmd path now has USRC_TEST at the end of it.
5. Type in `cd ..`. This will move your terminal window back out of your folder.
   - OSX, Linux: Type `pwd` again and check it's doing what you want.
   - Windows: Your path should no longer have USRC_TEST at the end of it.
6. Try making another folder inside of USRC_TEST, using the commands above.
7. Make an empty file in your USRC_TEST folder. First `cd` until you reach USRC_TEST, then:
   - OSX,Linux: `touch newfile.txt` 
   - Windows: `type nul > newfile.txt`
8. Use the file explorer to check that everything is as you expect.

## 2.5 A few more things before we start
Type in:
```
git config --global user.name "YOUR_NAME"
git config --global user.email "MY_NAME@example.com"
```
This tells git who you are, for when you're working with others. You only need to do this once.

## 3 Your first git repository
Now, let's copy over this repository, to see how we can get files quickly using git.

> **repository**: A collection of files.  

1. Open a command window.
  - Windows: Type in 'cmd' into your start. If all goes well, a black cmd window should appear.
  - Linux: Type in 'terminal' into your start. If all goes well, a black terminal window should appear.
  - OSX: Type in 'terminal' into your launcher. If all goes well, a white terminal window should appear.
2. Type in `mkdir USRC_TEST`, then press Enter. This makes a folder (instead of dumping everything in your documents / home directory. You can move this later using explorer/nautilus/finder.) 

> **mkdir \<name\>**: Make a directory here.

3. Type in `cd USRC_TEST`, then press Enter. This moves your cmd/terminal's focus into the folder we just created.

> **cd \<name\>**: **C**hange the **D**irectory.

4. Click on the **BIG GREEN "Clone or Download" BUTTON** under the header. There will be a link in there. Copy it down.

5. Type into your command window: `git clone https://github.com/usydroboticsclub/intro.git`. (Yep, that's the link you just copied. You can `ctrl-v` it in on windows, or `ctrl-shift-v` on MacOS and Linux.

6. Press Enter. You should see something like this:

```
Cloning into 'intro'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 675 bytes | 51.00 KiB/s, done.
```

7. Look around, by typing `cd intro`, and then either `dir` (windows) or `ls` (macos or linux). You should see `README.md`, which is this file, and some other stuff. These are the same files that are in this repository, if you scroll to the top.

8. Take a look at `Completed.md` using your file explorer. Find the file and open it with notepad/textedit. 

9. Go back to your terminal and type in:
 - Windows: `type Completed.md`
 - Mac/Linux: `cat Completed.md`.
Is it the same?

10. `cd` back out to the `USRC_TEST` directory, and `mkdir MYFORK` and `cd MYFORK` in preparation for the next part.

And that's it! If you want to practice this, then why not try cloning some other stuff on github, like [this one](https://github.com/rick/roll). 

## 4 Getting started with github
You can use git with 2 computers directly, but chances are that you don't have two computers on hand; so instead we'll have to use github as a third party. Let's get you signed up to github.
1. Go here: https://github.com/
2. Sign up, in the top right corner.
3. That's it. Github is nice and easy.

## 5 Fork this repository
The polite way of making changes to a repository on github is to copy it to your own github repository. This is called forking, and happens ALL on github. 

1. If you're reading this, you should be able to see the `Fork` button in the top right corner. Press that button. 

> **Fork:** To create a copy of someone else's repository in your personal repository.

2. Once you've forked this repository, clone it using the steps in part 2, but make sure you're working in your personal directory (you should see yourname/intro up the top). Since this is your copy, you are the owner, so you can change it willy nilly. Let's go do that now.


## 5 Your first changes
Now, we'll make some changes to this very repository, and tell Git that we've done so.
1. Go back to your terminal window.
2. Open the folder by typing `explorer.exe .` (windows) or `nautilus .` (linux) or `finder .` (macosx)
3. Put your name on the end of `Completed.md` with your favourite text editor. I recommend getting [VSCode](https://code.visualstudio.com/) for all platforms.
4. Save your changes. 
5. Go back to your terminal window, and type in `git add .`. This tells git to look at all the changes you made, and prepare them for sharing. 
6. Now type in `git commit -m "Added my name"`. This tells git that you're sure you want to make these changes, and tells git to tell other people that these changes pertain to adding your name. (The `-m` stands for message. You must have a message with your changes, because git likes to **enforce** good coding practice.)
7. Now type `git push origin master`. This tells git to pass your changes to github. You may have to login using your github username and password (or your email and password).

> **git push \<remote_location\> \<branch\>** : Pass your work on to someone else. If they'll take it. 

8. Great! If you visit your forked repository now on github, you'll be able to see your new changes in your file.

## 6 Making a pull request
Now that you've made some changes to your local version of git, you'll want to make a pull request. 

> **pull request**: a polite way of asking a project owner to accept your changes.

1. Press the `Pull requests` tab on your own github repository.
2. Click `Submit a pull request`, then click the green button(s).
3. Email us, and we'll approve it.
4. Great! Your name is now on our list. Welcome to the club! And welcome to Github!

## 7 Make a repository
Ok, so now you can copy other people's repositories. But what if you want to make your own?
1. Go back to your terminal window. `cd` to USRC_TEST again. 
2. `mkdir` yourself a new directory, and `cd` into it.
3. Type in `git init .`. This tells git to start considering this directory as a repository.
4. Go to www.github.com, and make yourself a new repository, with the big `+` button in the top right corner. **DO** add a `README.md`, for the purposes of this exercise.
5. Type in `git remote add origin https://your_github_url`. This associates your new repository with the one in your github, since initially they don't know about each other.
6. Type in `git pull origin master`. This tells git to fetch the files from your github repository and put them on your computer. It's the opposite of `git push`. 

Note: you may experience an error here that looks something like this. ![alt text](https://github.com/usydroboticsclub/intro/blob/master/master_error.png)

If this is the case, then try `git pull origin main` instead (Git has some funny terminology for main and master). Then you'll want to switch to the main directory by typing `git checkout main`.

7. Type `ls` or `dir` again. You should now see the readme.md file on your computer.
8. Make a few changes to the readme.md. Maybe add a few new files in the same folder.
9. Type in `git add .` then `git commit -m "<some message>"` when you're done.
10. Finally, type `git push origin master`, and check that your changes are saved on the cloud.


## 8 Key takeways
- Git is a tool for sharing files. Github is a place where files are stored.
- Some basic terminal commands for you: `mkdir` to make a directory, `cd` to change directories, and `dir` or `ls` to list the contents of your directory.
- `git clone <link>` to copy someone's repository
- `git add .` then `git commit -m "message"` to save your work.
- `git pull` to get a version from a repository.
- `git push origin master` to share your work with others.



## To add?
- Branches
- .gitignore
- Common errors
