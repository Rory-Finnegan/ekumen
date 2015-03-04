# Ekumen
A utility wrapper around ansible for managing playbooks, roles and dynamic inventory

## Why Ekumen?
The Ekumen were a inter-galactic political league/organization in [Ursula K. Le Guin's](http://en.wikipedia.org/wiki/Ursula_K._Le_Guin) [Hanish Cycle](http://en.wikipedia.org/wiki/Hainish_Cycle), who used the [ansible](http://en.wikipedia.org/wiki/Ansible) for interstellar communication. Since, this is where the term ansible first originated and ekumen is a CLI utility for ansible, it seemed fitting to continue the pattern.

## Usage
  * `ekumen init --playbook|role <name>`: Builds a template ansible playbook or role directory structure, similar to what ansible-role-manager did.
  * `ekumen invent <dynamic inventory>`: Generates a basic inventory file of hosts from the dynamic inventory based on your `ekumen.yml` config file
  * `ekumen install`: Installs third party roles into `./.installed-roles` and links them into `./roles` once again similar to ansible-role-manager, 
  but uses ansible-galaxy rather than trying to do its own dependency handling.
  * `ekumen status`: returns git status of the playbook, but also all repos in `./.installed-roles`
  * `ekumen diff`: same as ekumen status, but `git diff`
  * `ekuman run`: wraps `ansible-playbook` with the same parameters, but automatically uses a generated inventory file and appends any params in `ekumen.yml`
