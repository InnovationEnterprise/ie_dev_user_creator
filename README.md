# IE Dev User Creator

## Introduction

This is an extremely basic Ansible project that:

- ensures the existence of a `dev` user across multiple servers
- adds SSH keys of specified GitHub users to the `dev` account on each server
- creates the `/var/www` directory for servers and gives `dev` the access to it

## Usage

1. Install [Ansible](http://docs.ansible.com/).

2. Copy the `servers.sample` file to `servers` and add in your servers. Ensure that the user you SSH through is a sudo user e.g. `ubuntu` for AWS EC2.

3. (Optional) Copy `group_vars/servers.yml.sample` to `group_vars/servers.yml` and add GitHub users whose SSH keys you want added to the `dev` user.

4. Run the following from the project's directory:

    `ansible-playbook run.yml`
