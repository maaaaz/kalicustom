Kali custom
===========

Description
-----------
Some Kali VM builds with customizations

Additions
---------
Everything is documented in the [build workflow](https://github.com/maaaaz/Kalicustom/blob/main/.github/workflows/build.yml) but here is a quick summary:
- These packages (utilities, infosec tools etc.)
  - https://github.com/maaaaz/dotfiles/blob/master/debian_ubuntu_packages.txt
  - https://github.com/maaaaz/dotfiles/blob/master/kali_missing_packages.txt
  - Microsoft Sysmon and ProcDump for Linux
- Bash as default shell
- A friendlier .vimrc
- VMWare and VirtualBox compatibility
- Virtualbox permission fix by adding the `kali` to the `vboxsf` group
- A Python `venvcommon` virtualenv (in the root home), with common infosec Python packages
