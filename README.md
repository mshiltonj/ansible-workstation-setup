# Workstation setup
This is a bootstrap, public ansible repo for setting up a new linux workstation.

These ansible playbooks are to be ran on a base 18.04 ubuntu install. (It may work on others, let me konw)
The only other dependencies needed to get start are system git and ansible. 

I run this after intializing a new machine with vagrant. I login as the vagrant user, run the below commands,
then I can switch to my user and disable the vagrant account. 

I usually re-clone this repo for my main account to make any needed sytem changes with this ansible playbook.


# Installation

    sudo apt install git ansible -y
    git clone git@github.com:mshiltonj/ansible-workstation-setup.git
    cd git@github.com:mshiltonj/ansible-workstation-setup.git
 
# Steps

## Install the latest ansible from the ppa
Run this command. It will upgrade ansible to 2.9+, including ansible galaxy

    ansible-playbook uprade-ansible.yml

## Install all the upgrades and new installations
Run this command. It installs... a lot. Docker from PPA, Git from PPA, vscode, chrome, others.

    ansible-playbook setup-workstation.yml

## Add and setup the primary user (that's you!)
Run this command. It create 
    ansible-playbook setup-primary-user.yml e user=<linux-login-name>

# Contributing

This is a very personal and personalized project for me, but if you like it have suggestions create an issue or  pull request.


