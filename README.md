if [[ -r "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh" ]]; then
  source "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh"
fi

getRecentDownload() {
    windowsDownloadsLocation="/mnt/c/Users/farid/Downloads"
    fileNameRecentDownload=$(ls -Art $windowsDownloadsLocation | tail -1)
    mv "$windowsDownloadsLocation/$fileNameRecentDownload" .
}

export PATH=$HOME/bin:/usr/local/bin:$PATH


export PATH="/home/faridguzmzn91/.local/bin:$PATH"
export PATH=/opt/homebrew/bin:$PATH
export PATH="/opt/homebrew/bin:$PATH"
export PATH=/usr/local/bin:$PATH


export PATH=/usr/.local/bin:$PATH


export PATH="/home/linuxbrew/.linuxbrew/bin:$PATH"
export PATH="/home/linuxbrew/.linuxbrew/sbin:$PATH"


export ZSH="$HOME/.oh-my-zsh"

ZSH_THEME="powerlevel10k/powerlevel10k"

# ZSH_THEME_RANDOM_CANDIDATES=( "robbyrussell" "agnoster" )

plugins=(git zsh-autosuggestions zsh-syntax-highlighting zsh-autocomplete fast-syntax-highlighting)

source $ZSH/oh-my-zsh.sh

[[ ! -f ~/.p10k.zsh ]] || source ~/.p10k.zsh

# Add RVM to PATH for scripting. Make sure this is the last PATH variable change.
export PATH="$PATH:$HOME/.rvm/bin"

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
