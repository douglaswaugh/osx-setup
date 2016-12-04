Setting up a new laptop
===

* Install iTerm2 with oh-my-zsh
    * Disable save/restore alternate screen in iTerm2
* Set up SSH
    * Instructions on [github][]
    * Add ssh key to keychain `ssh-add -K ~/.ssh/id_rsa`
* Install and update homebrew 
* Install and update rbenv
    * Install wget with homebrew `brew install wget`
    * Run `rbenv init` once and follow instructions
* Install and update bundler `gem install bundler`
* Install git from homebrew `brew install git`
* Add diff-highlight to git diff
    * ``git config --global core.pager `brew --prefix`/share/git-core/contrib/diff-highlight/diff-highlight | less``
* Install Tim Pope's [Pathogen][]

        mkdir -p ~/.vim/autoload ~/.vim/bundle && \
        curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim

* Create `~/.vimrc` and copy

        execute pathogen#infect()
        syntax on
        filetype plugin indent on

* Add paste from the clipboard functionality to vim (version 7.4+).  Copy to `~/.vimrc`

        set clipboard=unnamed

* Install VS Code
    * Add code to PATH by pressing `F1` then typing `Shell Command: Install 'code' command in PATH`

[github]: https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-mac "generate new ssh key"
[Pathogen]: https://github.com/tpope/vim-pathogen "Pathogen"