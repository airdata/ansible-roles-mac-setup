# macOS setup via Ansible

<p align="center">
  <img width="200" src="./images/sonoma.png">
  <img width="140" src="./images/ansible.png">
</p>

- This is my personal macOS setup using Ansible and will be updating it as I go along. (Currently compatible for macOS Sonoma 14.0)

# 1.Install

1. Make sure you have xcode-select installed: `xcode-select --install`
2. Install Ansible:
   1. export PATH="$HOME/Library/Python/3.9/bin:/opt/homebrew/bin:$PATH"
   2. sudo pip3 install ansible --upgrade pip
   3. pip3 install ansible
3. Clone this repo
4. Run `ansible-playbook main.yml -r requirements.yml` inside this directory. Enter your account password when prompted (for sudo access).
5. Run `ansible-playbook main.yml --ask-become-pass` inside this directory. Enter your macOS account password when prompted for the 'BECOME' password.

# 2. Install:
## Xcode 

```sh
xcode-select --install
xcodebuild -license accept
softwareupdate --install-rosetta
```

## Ansible

```
sudo python3 -m pip install --upgrade pip
sudo python3 -m pip install ansible
```

## Pre-requisites

- Set machine
- Github access token

## Install

```
ansible-playbook main.yaml --ask-become-pass
```

## Post install

- Set password on ssh key

## TODO

- more zshrc stuff
- iterm colors
- zsh theme
- zprofile

