# Setup ZSH

## Termux
### Install ZSH
```
pkg install zsh
```
### Make ZSH default shell
```
chsh -s zsh
```
### Install Oh My ZSH
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k && sed -i 's+ZSH_THEME=".*"+ZSH_THEME="powerlevel10k/powerlevel10k"+g' ~/.zshrc
```
### Plugin ZSH :
#### 1. Auto suggestions
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
#### 2. Syntax highlighting
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
#### 3. Completions
```
git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions
```
#### 4. Add plugins
```
sed -i 's+plugin(.*)+plugin(git zsh-autosuggestions zsh-syntax-highlighting zsh-completions)+g'
```
### Install Colorls
```
pkg install colorls
```
#### Setup shortcut
```
sed "/# Example aliases/a alias la='colorls -a --sd'" ~/.zshrc
sed "/# Example aliases/a alias la='colorls -la --sd'" ~/.zshrc
```
