# Ansible Playbook for a fresh start

This Playbook is for setting up a new Kali VM with my customizations and Settings. For now it just has following contents:

###  Kali Settings

- Installing German Keyboard `qwertz` 
- Sets the keyboard setting as primary 


### Customize-Terminal

- Common CLI tools installed (zsh, git, curl/wget, gpg, bat, grc, fzf, tmux)
- kali user’s default shell switched to Zsh
- `Oh My Zsh` installed into /home/kali/.oh-my-zsh 
- `eza` (modern ls replacement) installed
- Custom `.zshrc` file for using with `plugins` and `fzf`
- `tmux.conf` updated (from Chris Alup & Ham Vocke)
-  Installs Hack Nerd Font 

## Installation 



If you want to disable some plays like `installing keyboard` then just make a comment in the `main.yml`.

Like 
```bash
#     - role: "roles/kali-settings"
```
Make sure, that your `kali` is patched! 

```bash
sudo apt-get update && apt-get upgrade -y
```

- Install Ansible
```bash
sudo apt install ansible
```

- Download repository
```bash
git clone https://github.com/WindWaker-IT/ansible_kali_vm.git
cd ansible_kali_vm
```
- Execute main.yml as `sudo`

```bash
sudo ansible-playbook main.yml
```

- Restart Terminal but better a full restart


### Bloodhound

After running the whole playbook, `bloodhound-cli` is installed and the password is in `/root/bloodhound_ce_admin_password.txt`
You can start and stop the container via `bloodhound-cli containers start/stop`

Make sure to change the password after inital execution.

## Contributing

Pull requests are welcome.

Thanks, I have a lot of configurations and information from you:

- https://github.com/neosprings
- https://github.com/hamvocke
- https://github.com/ippsec
- https://github.com/ohmyzsh/ohmyzsh




## License

[MIT](https://choosealicense.com/licenses/mit/)