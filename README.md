# 自用ZSH配置

### 安装ZSH及其他软件包
ArchLinux
```
sudo pacman -S zsh git curl
```
Debian/Ubuntu
```
sudo apt install zsh git curl
```

### 安装oh-my-zsh
```
sh -c "$(curl -fsSL https://install.ohmyz.sh/)"sh -c "$(curl -fsSL https://install.ohmyz.sh/)"
```

### 拉取主题和插件
```
git clone --depth=1 https://gitee.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
git clone --depth=1 https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone --depth=1 https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
### 配置.zshrc
```
sed -i 's/^ZSH_THEME="robbyrussell"$/ZSH_THEME="powerlevel10k\/powerlevel10k"/' ~/.zshrc
sed -i 's/^plugins=(git)$/plugins=(git z zsh-autosuggestions zsh-syntax-highlighting sudo)/' ~/.zshrc
source ~/.zshrc
```
