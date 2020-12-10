## centos install
1. install zsh
> yum install -y zsh

2. set to default shell, then relogin the shell to take effect.
> chsh -s /bin/zsh

3. install oh-my-zsh
> wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | sh

4. zsh plugins
> git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
> git clone git://github.com/zsh-users/zsh-syntax-highlighting $ZSH_CUSTOM/plugins/zsh-syntax-highlighting

4. add to .zshrc
> plugins=(
  git
  zsh-autosuggestions
  zsh-syntax-highlighting
)
> ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE='fg=yellow'
