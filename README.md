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

## Contributing

Pull requests are welcome.

Thanks, I have a lot of configurations and information from you:

- https://github.com/neosprings
- https://github.com/hamvocke
- https://github.com/ippsec
- https://github.com/ohmyzsh/ohmyzsh




## License

[MIT](https://choosealicense.com/licenses/mit/)