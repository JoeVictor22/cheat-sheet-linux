# Packages/programs to install after a clean install of manjaro/arch

## Basic

### Update kernel

```console
mhwd-kernel -l
mhwd-kernel -li
mhwd-kernel -i linux517
```

### Update packages

```console
sudo pacman -Syu
```

### Packages/programs

```console
sudo pacman -S base-devel
sudo pacman -Sy gcc
sudo pacman -S make
sudo pacman -S snapd
sudo pacman -S emacs
sudo pacman -S vim
sudo pacman -S net-tools
sudo pacman -S gnu-netcat
sudo pacman -S iputils
sudo pacman -S htop
sudo ln -s /var/lib/snapd/snap /snap
sudo snap install code --classic
sudo snap install opera
sudo snap install chromium
```

## Compilers/runtime

### Node/python

```console
sudo pacman -S pyenv
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
# fix path and .zshrc before using nvm
nvm install node
```

### Java

```console
sudo pacman -S jre-openjdk-headless jre-openjdk jdk-openjdk openjdk-doc openjdk-src
```

### Rust

```console
sudo pacman -S rustup
rustup default stable
```

### Gcloud/k8s/helm

```console
sudo snap install google-cloud-sdk --classic
sudo snap install helm --classic
sudo snap install terraform --candidate
sudo snap install kubectl --classic 
```

## Git

### Git ssh

```console
ssh-keygen -t ed25519 -C "your_email@example.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa # ou o nome da sua chave
cat .ssh/id_rsa.pub  # copiar chave para adicionar ao github
```

## Others

### Leisure

```console
sudo snap install discord
sudo snap install spotify --classic
```

### Doom-emacs

```console
git clone --depth 1 https://github.com/hlissner/doom-emacs ~/.emacs.d
~/.emacs.d/bin/doom install
echo 'export PATH="$HOME/.emacs.d/bin/:$PATH"' >> .zshrc
exec $SHELL
doom sync
doom upgrade
doom build
```
