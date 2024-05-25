``` bash
                '.88888888:.
                88888888.88888.
              .8888888888888888.
              888888888888888888
              88` _`88`_  `88888
              88 88 88 88  88888
              88_88_::_88_:88888
              88:::,::,:::::8888
              88`:::::::::'`8888
             .88  '::::'   '8:88.
            8888            `8:888.
          .8888'              888888.
         .8888:..  .::.  ...:'8888888:.
        .8888.'     :'     `'::`88:88888'
       .8888        '         `.888:8888.
      888:8         .           888:88888
    .888:88        .:           888:88888:
    8888888.       ::           88:888888
    `.::.888.      ::          .88888888
   .::::::.888.    ::         :::`8888'.:.
  ::::::::::.888   '         .::::::::::::'         _ _                         _                      _             _ 
  ::::::::::::.8    '      .:8::::::::::::.'        | (_)                      | |                    (_)           | |
 ':::mehdi::::::.        .:888:::::::::::::'        | |_ _ __  _   ___  __     | |_ ___ _ __ _ __ ___  _ _ __   __ _| |
 :::::::::::::::88:.__..:88888:::::::::::'          | | | '_ \| | | \ \/ /     | __/ _ \ '__| '_ ` _ \| | '_ \ / _` | |
  `'.:::::::::::88888888888.88:::::::::'            | | | | | | |_| |>  <      | ||  __/ |  | | | | | | | | | | (_| | |
        `':::_:' -- '' -'-' `':_::::'`'             |_|_|_| |_|\__,_/_/\_\      \__\___|_|  |_| |_| |_|_|_| |_|\__,_|_|
```



Thisvrepository named Terminal_Commands, which contains a comprehensive collection of terminal commands and instructions for various tasks related to Git, GitHub, VSCode, Anaconda, and Linux commands.

## Table of Contents

- [Git & GitHub](#git--github)
  + [Git cheat sheet](#Git-cheat-sheet)
  + [Git Usage](#git-usage)
- [VSCode](#VSCode)
- [Anaconda](#anaconda)
- [Linux Commands](#linux-commands)
- [Bash Files](#Bash-Files)

<html>
  Git & GitHub
<head>
</head>
<body>
  <h3>Git cheat sheet</h3>
    <h4>SETUP</h4>
  <p>Configuring user information used across all local repositories</p>
  <table>
    <tr>
      <td class="command">git config --global user.name “[firstname lastname]”</td>
      <td class="description">set a name that is identifiable for credit when review version history</td>
    </tr>
    <tr>
      <td class="command">git config --global user.email “[valid-email]”</td>
      <td class="description">set an email address that will be associated with each history marker</td>
    </tr>
    <tr>
      <td class="command">git config --global color.ui auto</td>
      <td class="description">set automatic command line coloring for Git for easy reviewing</td>
    </tr>
  </table>
  <h4>SETUP & INIT</h4>
  <p>Configuring user information, initializing and cloning repositories</p>
  <table>
    <tr>
      <td class="command">git init</td>
      <td class="description">initialize an existing directory as a Git repository</td>
    </tr>
    <tr>
      <td class="command">git clone [url]</td>
      <td class="description">retrieve an entire repository from a hosted location via URL</td>
    </tr>
  </table>
  <h4>STAGE & SNAPSHOT</h4>
  <p>Working with snapshots and the Git staging area</p>
  <table>
    <tr>
      <td class="command">git status</td>
      <td class="description">show modified files in working directory, staged for your next commit</td>
    </tr>
    <tr>
      <td class="command">git add [file]</td>
      <td class="description">add a file as it looks now to your next commit (stage)</td>
    </tr>
    <tr>
      <td class="command">git reset [file]</td>
      <td class="description">unstage a file while retaining the changes in working directory</td>
    </tr>
    <tr>
      <td class="command">git diff</td>
      <td class="description">diff of what is changed but not staged</td>
    </tr>
    <tr>
      <td class="command">git diff --staged</td>
      <td class="description">diff of what is staged but not yet commited</td>
    </tr>
    <tr>
      <td class="command">git commit -m “[descriptive message]”</td>
      <td class="description">commit your staged content as a new commit snapshot</td>
    </tr>
  </table>

  <h4>BRANCH & MERGE</h4>
  <p>Isolating work in branches, changing context, and integrating changes</p>
  <table>
    <tr>
      <td class="command">git branch</td>
      <td class="description">list your branches. a * will appear next to the currently active branch</td>
    </tr>
    <tr>
      <td class="command">git branch [branch-name]</td>
      <td class="description">create a new branch at the current commit</td>
    </tr>
    <tr>
      <td class="command">git checkout</td>
      <td class="description">switch to another branch and check it out into your working directory</td>
    </tr>
    <tr>
      <td class="command">git merge [branch]</td>
      <td class="description">merge the specified branch’s history into the current one</td>
    </tr>
    <tr>
      <td class="command">git log</td>
      <td class="description">show all commits in the current branch’s history</td>
    </tr>
  </table>
  <h4>INSPECT & COMPARE</h4>
  <p>Examining logs, diffs and object information</p>
  <table>
    <tr>
      <td class="command">git log</td>
      <td class="description">show the commit history for the currently active branch</td>
    </tr>
    <tr>
      <td class="command">git log branchB..branchA</td>
      <td class="description">show the commits on branchA that are not on branchB</td>
    </tr>
    <tr>
      <td class="command">git log --follow [file]</td>
      <td class="description">show the commits that changed file, even across renames</td>
    </tr>
    <tr>
      <td class="command">git diff branchB...branchA</td>
      <td class="description">show the diff of what is in branchA that is not in branchB</td>
    </tr>
    <tr>
      <td class="command">git show [SHA]</td>
      <td class="description">show any object in Git in human-readable format</td>
    </tr>
  </table>
  <h4>TRACKING PATH CHANGES</h4>
  <p>Versioning file removes and path changes</p>
  <table>
    <tr>
      <td class="command">git rm [file]</td>
      <td class="description">delete the file from project and stage the removal for commit</td>
    </tr>
    <tr>
      <td class="command">git mv [existing-path] [new-path]</td>
      <td class="description">change an existing file path and stage the move</td>
    </tr>
    <tr>
      <td class="command">git log --stat -M</td>
      <td class="description">show all commit logs with indication of any paths that moved</td>
    </tr>
  </table>
  <h2>IGNORING PATTERNS</h2>
  <p>Preventing unintentional staging or commiting of files</p>
  <table>
    <tr>
      <td class="command">logs/
*.notes
pattern*/</td>
      <td class="description">Save a file with desired paterns as .gitignore with either direct string 
matches or wildcard globs</td>
    </tr>
    <tr>
      <td class="command">git config --global core.excludesfile [file]</td>
      <td class="description">system wide ignore patern for all local repositories</td>
    </tr>
  </table>
  <h4>SHARE & UPDATE</h4>
  <p>Retrieving updates from another repository and updating local repos</p>   
  <table>
    <tr>
      <td class="command">git remote add [alias] [url]</td>
      <td class="description">add a git URL as an alias</td>
    </tr>
    <tr>
      <td class="command">git fetch [alias]</td>
      <td class="description">fetch down all the branches from that Git remote</td>
    </tr>
    <tr>
      <td class="command">git merge [alias]/[branch]</td>
      <td class="description">merge a remote branch into your current branch to bring it up to date</td>
    </tr>
    <tr>
      <td class="command">git push [alias] [branch]</td>
      <td class="description">Transmit local branch commits to the remote repository branch</td>
    </tr>
    <tr>
      <td class="command">git pull</td>
      <td class="description">fetch and merge any commits from the tracking remote branch</td>
    </tr>
  </table>
  <h2>REWRITE HISTORY</h2>
  <p>Rewriting branches, updating commits and clearing history</p>
  <table>
    <tr>
      <td class="command">git rebase [branch]</td>
      <td class="description">apply any commits of current branch ahead of specified one</td>
    </tr>
    <tr>
      <td class="command">git reset --hard [commit]</td>
      <td class="description">clear staging area, rewrite working tree from specified commit</td>
    </tr>
  </table>
  <h4>TEMPORARY COMMITS</h4>
  <p>Temporarily store modified, tracked files in order to change branches</p>
  <table>
    <tr>
      <td class="command">git stash</td>
      <td class="description">Save modified and staged changes</td>
    </tr>
    <tr>
      <td class="command">git stash list</td>
      <td class="description">list stack-order of stashed file changes</td>
    </tr>
    <tr>
      <td class="command">git stash pop</td>
      <td class="description">write working from top of stash stack</td>
    </tr>
    <tr>
      <td class="command">git stash drop</td>
      <td class="description">discard the changes from top of stash stack</td>
    </tr>
  </table>
<h3>Git Usage:</h3>

- **Creating a Repository**

   To create a new repository on GitHub, go to your profile page and click on the green "New" button.

- **set Git configuration**

  To set up github on the local git, open your terminal or command prompt and run the following commands:
  ```bash
  git config --global user.name “-------”
  git config --global user.email “------”
  ```
- **set Git configuration**

  To check your github configuration on the local git, run the following commands:
  ```bash
  git config --list
  ```

- **Cloning a Repository**
  
  To clone a repository, open your terminal or command prompt and run the following command:
  ```bash
  git clone git@github.com:username/repository.git
  ```
- **connect to a remote repository on GitHub**

  Run this git command to connect your local Git repository to a remote repository on GitHub.
  ```bash
  git remote add origin git@github.com:username/repositoryname.git
  ```
- **Adding a File to the Repository**

  To add a file to the repository, first make sure the file is in the correct directory. Then, open your terminal or command prompt and navigate to the directory where the file is located. Finally, run the following command:
  ```bash
  git add "filename"
  ```
- **Removing a File from the Repository**

  To remove a file from the repository, first make sure the file is in the correct directory. Then, run the following command:
  ```bash
  git rm --cached "filename"
  ```
- **Commiting Changes**

  After adding/removing the file, you can commit the changes to the repository with the following command:
  ```bash
  git commit -m "commit message"
  ```
- **Pushing Changes to GitHub**

  To push the changes to the GitHub repository, run the following command:
  ```bash
  git push origin master
  ```
- **Update your repo to the latest changes**

  If you already have a local copy of the repository and you want to update it, you can use the git pull command. This command fetches changes from the remote repository and merges them into your local branch.
  ```bash
  git pull origin main
  ```
  ```bash
  git pull git@github.com:username/repository.git master
  ```
- **Initializing a new repository**

  To create a new repository
  ```bash
  git init
  ```
- **Creating a New Branch**

  To create a new branch, run the following command:
  ```bash
  git checkout -b branchname
  ```

- **Switching Between Branches**

  To switch between branches, run the following command:
  ```bash
  git checkout branchname
  ``` 
- **current status of your working directory**

  This command shows you which files have been modified, staged, or deleted and the brach you are currently on. Additionally, it will show you any conflicts that may have arisen during a merge or rebase.
  ```bash
  git status
  ``` 
- **Merging Branches**

  To merge a branch into the master branch, first switch to the master branch and then run the following command:
  ```bash
  git merge branchname
  ```
  ```bash
  git merge branchname --no-edit -m "commit message"
  ```
- **Deleting a Branch**

  To delete a branch, run the following command:
  ```bash
  git branch -d branchname
  ``` 
- **view the commit history**

  This will display a list of all the commits made to the repository, including the author, date, and commit message.
  ```bash
  git log
  ```
## VSCode

- **Open VSCode using terminal**

  To open VSCode simply write:
  ```bash
  code
  ```
- **Open a file using VSCode**

  To open a file using VSCode simply write:
  ```bash
  code [filename]
  ```
## Anaconda
- **Installing Anaconda**

  To install Anaconda, follow these steps:

  Download the Anaconda installer for your operating system from the [official Anaconda distribution page](https://www.anaconda.com/products/distribution).
  Run the installer and follow the on-screen instructions.
- **Create a new environment**

  To create a new environment, run the following command:
  ```bash
  conda create --name myenv
  ```
  Replace myenv with the name you want to give to your environment.
- **Activate an environment**

  To activate an environment, run the following command:
  ```bash
  conda activate myenv
  ```
- **Install packages in the environment**

  A YAML environment file is a text file that specifies the packages and dependencies for an environment. To use a YAML environment file, create a file named environment.yml with the following content:
  ```bash
      name: myenv
      dependencies:
         - anaconda
         - python=3.8
         - pip
      - pip:
         - package1
         - package2
  ```
  Replace myenv with the name of your environment, and package1 and package2 with the names of the packages you want to install.
- **create an environment using the YAML file**
   
  To create an environment from the YAML file, run the following:
  ```bash
  conda env create -f environment.yml
  ```
- **Updating an Environment**

  To update an environment from the YAML file, run:
  ```bash
  conda env update -f environment.yml
  ```
  To update an environment, run:
  ```bash
  conda update --all --name myenv
  ```
  Replace myenv with the name of your environment.
- **Viewing a List of Your Environments**

  To view a list of all your environments, run:
  ```bash
  conda env list
  ```
  This will display a list of all your environments, along with their names and paths.

## Linux Commands
- **printing working directory**

  To print the path of the working directory, starting from the root
  ```bash
  pwd
  ```
- **Creating a New Directory**

  To create a new directory, run the following command:
  ```bash
  mkdir [directoryname]
  ```

- **Changing the Current Directory**

  To change the current directory, run the following command:
  ```bash
  cd [directoryname]
  ```
  To change the current directory to parent directory, run the following command:
  ```bash
  cd ..
  ```
  To change the current directory to root directory, run the following command:
  ```bash
  cd .
  ```
- **Listing the Contents of a Directory**

  To list the contents of a directory, run the following command:
  ```
  ls
  ```
- **Creating a New File**

  To create a new file, run the following command:
  ```bash
  touch [filename]
  ```
- **editing the file**

  To open and edit a file, run the following command:
  ```
  vi [filename]
  ```
- **Disk uusage**

  To analyze and report on disk usage within directories and files, execute the following command:
  ```
  du [directory/file]
  ```
- **Viewing the Contents of a File**

  To view the contents of a file, run the following command:
  ```
  cat [filename]
  ```
- **copy file**
  
  To copy a file, run the following command:
  ```
  cp [Source_file] [Destination_file]
  ```  
- **Deleting a File or Directory**

  To delete a file or directory, run the following command:
  ```bash
  rm -rf [filename]
  ```  
- **history of executed command**

  To view previously executed this command:
    ```
    history
    ```
- **view date and time**

  To view current date and time executed this command:
    ```
    date
    ```
- **view calender**

  To view specific month in a year executed this command:
  ```
  cal [month][year]
  ```
  To view current month in a year executed this command:
  ```
  cal
  ```
  To view full year executed this command:
  ```bash
  cal -y
  ```  
- **Generate a new SSH key pair**

  This following command will generate a new SSH key pair. It creates a RSA key pair and saves the private key to a file named "id_rsa" in the "~/.ssh" directory, and it saves the public key to a file named "id_rsa.pub" in the same directory.
  ```bash
  ssh-keygen -t rsa
  ```
  ```bash
  ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
  ```
  This command will generate a new SSH key pair. It creates a 4096-bit RSA key pair and saves the private key to a file named "id_rsa" in the "~/.ssh" directory, and it saves the public key to a file named "id_rsa.pub" in the same directory. The -C flag is used to add a comment, which is useful for identification purposes.
- **Searching for a File or Directory**
  
  To search for a file or directory, run the following command:
  ```
  find / -name "filename" 2>/dev/null
  ```

- **Downloading a File**
  
  To download a file, run the following command:
  ```
  wget fileurl
  ```

- **Extracting a Zip File**
  
  To extract a zip file, run the following command:
  ```
  unzip filename.zip
  ```

- **Compressing a Directory**

  To compress a directory into a zip file, run the following command:
  ```
  zip -r filename.zip directoryname
  ```

- **Moving a File or Directory**

  To move a file or directory, run the following command:
  ```
  mv filename destination
  ```

- **Renaming a File or Directory**
  
  To rename a file or directory, run the following command:
  ```
  mv oldfilename newfilename
  ```

- **Updating the System**
  
  To update the system, run the following command:
  ```
  sudo apt-get update && sudo apt-get upgrade
  ```

- **Checking the System's Uptime**
  
  To check the system's uptime, run the following command:
  ```
  uptime
  ```
## Bash Files
- **Creating a Bash File**
  
  To create a bash script file with the .sh extension. For example, "my_script.sh" Add a shebang line at the beginning of the script to specify the interpreter. In this case, we will use bash.
  ```bash
  #!/user/bin/bash
  ```
  Write your script commands under the shebang line. Each command should be on a new line. For example, let's print "Hello, World!" and list the files in the current directory.
  ```bash
  #!/user/bin/bash

  echo "Hello, World!"

  ls
  ```
  Save your script file.

  Open a terminal and navigate to the directory where your script file is located. Give the script file execute permissions by running the following command:

  ```bash
  chmod +x my_script.sh
  ```
  Now you can run your script by executing the following command:

  ```bash
  ./my_script.sh
  ```
  This will execute your script and display the output in your terminal.

  Remember to replace my_script.sh with the actual name of your script file.
    - EXAMPLE:
      ```bash
      #!/user/bin/bash
      greeting = "welcome"
      user = $(whoami)
      day = $(date + %A)
      echo "greeting back $user! Today is $day, which is the best day of the entire week!"
      echo "your bash shell version is $BASH_VERSION. Enjoy!"
      ```
