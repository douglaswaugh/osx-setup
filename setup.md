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
* Install and update bundler
* Install git from homebrew
* Install Tim Pope's [Pathogen][]

        mkdir -p ~/.vim/autoload ~/.vim/bundle && \
        curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim

* Create `~/.vimrc` and copy

        execute pathogen#infect()
        syntax on
        filetype plugin indent on

* Add paste from the clipboard functionality to vim (version 7.4+).  Copy to `~/.vimrc`

        set clipboard=unnamed

[github]: https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-mac "generate new ssh key"
[Pathogen]: https://github.com/tpope/vim-pathogen "Pathogen"