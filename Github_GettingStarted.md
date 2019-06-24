```
                            *@%&&&=--                      
       .@%.                  .&****(@                      
         &*/#&*               (#****&                      
         (#***&*               @***(%                      
          &**#,                %(**&                       
          @/*&                 .%**&                       
          (((%                  &*/@                       
          ,#%.  (@@*            @*(& .#@@%((%@#            
          .#(@@@@%/*          ,%@*(@#.                     
    ,&@&&@@#@        /&@@@@@&   &*#(                       
@@@%#%@.  ##@                 *%**/@                       
         ##*&@               @(#@(#@@&                     
        (%*/@ @@           (%/&.,#%,.&&%                   
       #&%@    @@*      .&/(&  .#%,  @(#%                  
      &%@ .%@    /#     @(*&*   .#%,   #%*%&               
     @@.  .%@         @(*#%     .#%*     &**#@             
   %@.    ,%@       @#*(@       .##/      @(**/&/          
 ,%       /#@     @(*#@         ,###       /#****(&/       
          #(@   @@&@*           *((%        ,&******#@/    
          @/@                   /((@          .%@&%#(((#@@*
          &*&                   ((/@                       
         @/*&                   #/*@                       
            &                   &/*&                       
            @           @@@%,   &/*%.                      
                          .@%/*****##                      
                              ,&&%(#%                      
```

Step 1 - Login to Github and fork the repository
You get a copy of the repo to your own account!

Get Windows Terminal - Better version of command prompt
Get Windows Subsytems for Linux
Enable subsytem for Linux - Via Command Prompt

Grab Ubuntu 18.04 LTS - Long Term Support

ctrl-a - Start of line
ctrl-k - Delete all from pointer to end
ctrl-Left/right - jump by word
history - Shows prior used commands - For as long as recorded

From command prompt
  - Type 'bash' - basically opens a bash terminal
  - Type powershell - basically opens powershell

Configuration Management

Use chocalatey on Windows
https://chocolatey.org/
Windows Package Manager
  - Maintain list of packages

Salt, 		Chef, 	Ansible, 	Puppet
(Python + YAML), 	Ruby, 	Ruby, 		Python

https://puppet.com/
https://www.saltstack.com/ - Has an event bus - All connected machines push to the bus, salt master can react

git checkout -b <name> - Where name is
YourUsername-WhatYou'reDoing
Organization specific rules, generally - find from the org how they want branches named
Might also correspond to bug numbers or other identifiers
In point of fact, name has no real impact except to the professional standards, does not alter behavior of code

esc to escape write mode
shift ; (:) to enter command line mode
Then enter commands to execute in order of exectuion (wq) for write->quite

Download the vi cheat sheet
https://vim.rtorr.com/

Emacs
https://www.gnu.org/software/emacs/

sudo apt install emacs25-nox - nox version denotes no Windows X functionality, is lighter weight

Set up Keybase to manage passwords
https://www.youtube.com/watch?v=8_L6XljCZzA

Secret seeds 2FA tokens
https://www.nongnu.org/oath-toolkit/
MFA

Never enter a secret or key on the command line - Get's dumped into the audit history/log

To handle a secret:

Place the secret in a file on a flash drive
Connect the flash drive to a trusted machine
Encrypt the secret
Pass that as a file argument via command line so it never shows up in audit log!

OR

Use Pass application to handle the secrets

git add <filename> - Stages it for git commit
Stages for commit - allows isolation of changes in case there's more than you want to send
git add . - Adds anything that has diffed from the head of the branch - Basically adds everything

git init - Makes a new repository
git status

zhshell - Can add shortcuts for common commands (ga for git add or gc for git commit)
  Basically aliasing, can also be done in bash (?)

$ alias - List of all aliases in the environment
http://kurtdowswell.com/software-development/git-bash-aliases/
Can paste content into gitconfig file to expand or adjust aliasing

https://coderwall.com/p/_-ypzq/git-bash-fixing-it-with-alias-and-functions

alias | grep <command>
Prints out just what the <command> alias is

git log --oneline --decorate --graph --all
Or just glog if you have the gitconfig configured properlike

ONE TIME SETUP
git config --global user.email "twhlum@gmail.com"
git config --global user.name "Teabeans"

git config --local user.email "professional@pro.pro"
git config --local user.name "Professional Lum"

Or vice versa if doing more pro work than freelance

At time of commit, use the global or local identity appropriately

$ git commit

Enter a description of the commit

NOTE: Change default editor to emacs

Can also do git commit -m <MESSAGE>
Where message is the description

git show

git commit -S
Signed with GPG key
Samish thing as PGP key

When generating a GPG key, treat it like your fingerprint
$ gpg --full -generate-key

Use RSA 4096 for highest compatibility with older systems

Key does not expire so you can use it forever

https://keybase.io/blog/encrypted-git-for-everyone

Change is commited to the LOCAL repository, must be pushed back to origin (TODO)
Repos can have multiple remotes configured for it
Repos can be, say, on both GitHub and GitLab

git push --set-upstream origin $(git branch | grep \* | awk {'print $NF'})
^^ - Queries the current branch name and uses that for the push

git checkout

Set up an SSH key
- Instead of committing via http: use SSH key
 - $ ssh keygen -t
Generates key in home directory
Go to Github, add an SSH key
Paste in public key
Validate identity
Key is registered with Github
PGP for signing files and verifying identity
SSH key just for connecting to GitHub

Get a commit with green Verified symbol via command line

