Setting up a new laptop
===

* Install iTerm2 with oh-my-zsh
    * Disable save/restore alternate screen in iTerm2
* Add paste from the clipboard functionality to vim (version 7.4+).  Copy to `~/.vimrc`

        set clipboard=unnamed

* Set up SSH
    * Instructions on [github ssh][]
    * Add ssh key to keychain `ssh-add -K ~/.ssh/id_rsa`
* Install and update homebrew 
* Install and update rbenv
    * Install wget with homebrew `brew install wget`
    * Run `rbenv init` once and follow instructions
* Install and update bundler `gem install bundler`
* Install git from homebrew `brew install git`
* Add diff-highlight to git diff
    * ``git config --global core.pager `brew --prefix`/share/git-core/contrib/diff-highlight/diff-highlight | less``
* Install [vim colors solarized][]
    * Install Tim Pope's [pathogen][]

            mkdir -p ~/.vim/autoload ~/.vim/bundle && \
            curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim

    * Clone vim colors solarized

            cd ~/.vim/bundle
            git clone git://github.com/altercation/vim-colors-solarized.git

    * Create `~/.vimrc`
    * Add vim colors solarized config to `~/.vimrc`

            execute pathogen#infect()
            syntax on
            filetype plugin indent on

    * Set colour scheme to Solarized Dark in iTerm profile preferences

        iTerm > Preferences... > Profiles > Colors > Color Presets... > Solarized Dark 

* Install VS Code
    * Add code to PATH by pressing `F1` then typing `Shell Command: Install 'code' command in PATH`

[vim colors solarized]: https://github.com/altercation/vim-colors-solarized "vim colors solarized"
[github ssh]: https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#platform-mac "generate new ssh key"
[pathogen]: https://github.com/tpope/vim-pathogen "Pathogen"