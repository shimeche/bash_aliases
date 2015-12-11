# bash_aliases

# for Ubuntu 12.04

#常用操作
alias grep='grep --color=auto'

alias l='ls -CF'

alias la='ls -A'

alias ll='ls -alF'

alias ls='ls --color=auto'

# apache 服務啟用、重起、停止
alias startapache='sudo service apache2 start'

alias restartapache='sudo service apache2 restart'

alias stopapache='sudo service apache2 stop'

# 設定apache組態檔
alias configapache='cd /etc/apache2/sites-available'

alias editapachecommonrule='sudo vim /etc/apache2/sites-available/common_rule'

alias editphpini='sudo vim /etc/php5/apache2/php.ini'

# 快速編輯aliases
這個版本需要先在~/.bashrc中include

from ~/.bashrc

if [ -f ~/.bash_aliases ]; then

   . ~/.bash_aliases
   
fi

alias editalias='vim ~/.bash_aliases'

alias rerunalias='source ~/.bashrc'

# 快速的設定proxy
`   setstproxy () {
      gsettings set org.gnome.system.proxy.socks host localhost
      gsettings set org.gnome.system.proxy.socks port 1235
      gsettings set org.gnome.system.proxy mode manual
      gsettings set org.gnome.system.proxy ignore-hosts "['localhost', '127.0.0.0/8', '*.cdn.hinet.net']"
   }
   alias setsshtunnlproxy='setstproxy'`

# 取消proxy
alias unsetsshtunnlproxy='gsettings set org.gnome.system.proxy mode none'

# 查看系統版本
alias osversion='lsb_release -a'
