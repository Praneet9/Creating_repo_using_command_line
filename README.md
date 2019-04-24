# Creating Repository using Command Line

Ever wondered if you could create a git repository and start working on your project without even firing up your browser? This is how you do it! You'll need [hub](https://github.com/github/hub) to do it.

## Installing [hub](https://github.com/github/hub)

#### MacOS

Use homebrew to install hub

```bash
$ brew install hub
```

#### Windows

Use [scoop](https://scoop.sh/) to install hub

```bash
$ scoop install hub
```

#### Linux

Unfortunately installing on linux is not straightforward due to broken packages. You'll need to build it manually.

```bash
$ wget https://github.com/github/hub/releases/download/v2.11.2/hub-linux-amd64-2.11.2.tgz
$ tar zvxvf hub-linux-amd64-2.11.2.tgz
$ sudo ./hub-linux-amd64-2.11.2/install
```

#### Autocompletion for ZSH (Optional)

Setup autocompletion for hub in zsh

```bash
$ mkdir -p ~/.zsh/completions
$ mv ./hub-linux-amd64-2.11.2/etc/hub.zsh_completion ~/.zsh/completions/_hub
$ echo "fpath=(~/.zsh/completions $fpath)" >> ~/.zshrc
$ echo "autoload -U compinit && compinit" >> ~/.zshrc
$ echo "eval "$(hub alias -s)"" >> ~/.zshrc
```

## Create repo using command line
Follow the commands below to create a repository on your github account from command line

```bash
$ mkdir GitHub_Repo
$ cd GitHub_Repo
$ git init
$ hub create
$ touch file_name.txt
$ git add .
$ git commit -m "Initial Commit"
$ git push --set-upstream origin master
```
