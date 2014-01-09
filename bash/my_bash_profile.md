'
export PATH=/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin:/usr/local/git/bin:/usr/X11/bin:/androidsdk/tools
export EXTLIBS_ROOT=/fronter/products/extlibs
export PATH="/usr/local/mysql/bin:$PATH"
export PATH=/opt/local/bin:/opt/local/sbin:$PATH
`
alias pho="open -a 'Adobe Photoshop CS6'"
alias ils="open -a 'Adobe Illustrator CS6'"

alias ss='/Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl'
alias jmeter='/fronter/apache-jmeter/bin/jmeter'
alias ls='ls -lhaG'
alias glg='git log --date-order --all --graph --format="%C(green)%h%Creset %C(yellow)%an%Creset %C(blue bold)%ar%Creset %C(red bold)%d%Creset%s"'
alias src='source ~/.bash_profile'
alias fless='ant less csscaches; terminal-notifier -message "Less:" "Compile finished"'

# lock computer
alias lock='/System/Library/CoreServices/"Menu Extras"/User.menu/Contents/Resources/CGSession -suspend'

# grep with color
alias grep='grep --color=auto'

# refresh shell
alias reload='source ~/.bash_profile'

# up 'n' folders
alias ..='cd ..'
alias ...='cd ../..'
alias ....='cd ../../..'
alias .....='cd ../../../..'


parse_git_branch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\[\033[0;36m\]\A:\[\033[01;34m\]\w\$\[\033[00m\]\$(parse_git_branch) "
source ~/.git-completion.bash
export PATH="/usr/local/bin:/usr/local/sbin:/usr/local/mysql/bin:/usr/local/share/npm/bin:$PATH"
`
