export PATH=/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin:/usr/local/git/bin:/usr/X11/bin:/androidsdk/tools
export EXTLIBS_ROOT=/fronter/extlibs
export PATH="/usr/local/mysql/bin:$PATH"
export PATH=/opt/local/bin:/opt/local/sbin:$PATH

alias pho="open -a 'Adobe Photoshop CS6'"
alias ils="open -a 'Adobe Illustrator CS6'"

alias ss='/Applications/Sublime\ Text\ 2.app/Contents/SharedSupport/bin/subl'
alias jmeter='/fronter/apache-jmeter/bin/jmeter'
alias ss='/Applications/Sublime\ Text\ 2.app/Contents/SharedSupport/bin/subl'
alias ls='ls -lhaG'
alias glg='git log --date-order --all --graph --format="%C(green)%h%Creset %C(yellow)%an%Creset %C(blue bold)%ar%Creset %C(red bold)%d%Creset%s"'
alias src='source ~/.bash_profile'
alias fless='ant less csscaches; terminal-notifier -message "Less:" "Compile finished"'

# lock computer
alias lock='/System/Library/CoreServices/"Menu Extras"/User.menu/Contents/Resources/CGSession -suspend'

# grep with color
alias grep='grep --color=auto'

# refresh shell
alias reload='source ~/.profile'

# up 'n' folders
alias ..='cd ..'
alias ...='cd ../..'
alias ....='cd ../../..'
alias .....='cd ../../../..'

source ~/.git-completion.bash

# enable the git bash completion commands
source ~/.git-completion.sh

parse_git_branch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\[\033[0;36m\]\A:\[\033[01;34m\]\w\$\[\033[00m\]\$(parse_git_branch) "


##
# Your previous /Users/jorgenjacobsen/.bash_profile file was backed up as /Users/jorgenjacobsen/.bash_profile.macports-saved_2013-11-05_at_09:58:22
##

# MacPorts Installer addition on 2013-11-05_at_09:58:22: adding an appropriate PATH variable for use with MacPorts.
export PATH=/opt/local/bin:/opt/local/sbin:$PATH
# Finished adapting your PATH environment variable for use with MacPorts.

irssi_notifier() {
    ssh jorgen@shell.fronter.net 'echo -n "" > ~/.irssi/fnotify; tail -f ~/.irssi/fnotify' | \
            while read heading message; do
            url=`echo \"$message\" | grep -Eo 'https?://[^ >]+' | head -1`;

            if [ ! "$url" ]; then
                terminal-notifier -title "\"$heading\"" -message "\"$message\"" -activate com.apple.Terminal;
            else
                terminal-notifier -title "\"$heading\"" -message "\"$message\"" -open "\"$url\"";
            fi;
        done
    }

