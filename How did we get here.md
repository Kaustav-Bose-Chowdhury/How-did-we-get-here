Before we start let us clear up a few terms:  
Git : It is an opensource version control system created by Linus Torvalds (The same Linus who created the Linux Kernel).  
Github : It is a company that provides code-repository service using Git for version control, offering features like bug tracking, task management, and AI-powered tools like GitHub Copilot.  
SSH (Secured Shell) : A protocol for securely connecting with remote severs. Other famous protocols are HTTPS, TCP, UDP.

First install git from their official website (Give website here)  
Follow the instructions as you are prompted. This step should not be much of a hassle. Follow any tutorial if you want.  
The real "fun" starts when you mess up.

After git bash is installed you should open it. You should find yourself face-to-face with "THE TERMINAL" (Its not that scary).  
To start we must create a new repository

To convert a directory to git repository open git bash in that directory, then `git init`.

To check which files are being tracked and which files are not tracked use `git status`.

To add files for tracking:  
- use `git add <filename>` to add a specific file for tracking. Example : `git add example.txt` or `git add "first file.txt"`
- use `git add <path to the file>` to add a file having  a certain path for tracking. Example : `git add dir1/file1.txt`
- use `git add <file1> <file2> ...` to add multiple files for tracking
- use `git add *.txt` to add all files of a certain extension for tracking
- use `git add dir1/*` to add all files of a certain directory for tracking
- use `git add .` or `git add -A` or `git add --all` to add all files for tracking.

(Tracking and staging are almost equivalent terms)

Sometimes you want to ignore certain files from your git history like log files or database files. You do not want your sensitive information to end up forever in a public repository.  
For that we add a special file called the git ignore file.  
To create a git ignore file use `touch .gitignore`.  
Open the gitignore file in a text editor of your choice.  
- add `<filename>` to ignore a file with that name. Example : `hello.txt` ignores any hello.txt file present in that repository
- add `*.txt` to ignore all text files
- add `dir1/*` to ignore all files in dir1
- add `dir1/*.txt` to ignore all text files in dir1

To commit all the tracked/staged changes use `git commit -m "Any message you want to put here"`. The message you put in your commit will be public so preferably put something that reflects the changes you have made. Do not put a generic  message.

After that you want to push your changes to the remote repository.  
But before doing that you would need to connect to the remote repository using SSH. How to do that is discussed later.  
After you have setup SSH connection use `git remote add origin <ssh path of the remote repository>` to add remote origin to your `git`.
>Note : origin is just the standard name of the pointer to the remote repository. In practice you can have any name.

After that use `git push origin master` to push your repository to the remote repository.