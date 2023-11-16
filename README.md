**Ofek Shani's Setup Tools for new Linux Environments.**


- use 'chmod u+x <scriptname>' where scriptname is the file to run.
- to add a new script to the path open up .bashrc and copy 'export PATH=$PATH:$HOME/<directory>'.
Then, type in 'source .bashrc' to reload the program. Your script should then be in the path.

**Aliases to add**
 - `alias gohome="cd ~"`
 - `alias lsl="ls -lah"`
 - `alias cd..="cd .."`

**Script Descriptions:**

*gl_login.sh:*
  Initiates the Great Lakes Cluster login process. Must be on-campus to use.
  usage: `gl_login.sh <uniqname>`
  setup: add script to /bin. (requires that bin be on the PATH).

*ohmyposh_install.sh*
  Installs Oh My Posh (terminal prompt customization tool) in a new directory within bin.
  setup: Add lines `PATH=$PATH:$HOME/bin/oh-my-posh` and 
    
  
*miniconda install process*
  setup: run the following 4 lines of code in home:
    `mkdir -p ~/miniconda3`
    `wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh`
    `bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3`
    `rm -rf ~/miniconda3/miniconda.sh`
    Then add `PATH=$PATH:$HOME/miniconda/bin` to .bashrc.
    finally, run `~/miniconda3/bin/conda init bash` and restart the editor.
