Kali custom
===========

Description
-----------
Some Kali VM builds with customizations

Additions
---------
Everything is documented in the [build workflow](https://github.com/maaaaz/Kalicustom/blob/main/.github/workflows/build.yml) but here is a quick summary:
- These packages (utilities, infosec tools etc.):
  - https://github.com/maaaaz/dotfiles/blob/master/debian_ubuntu_packages.txt
  - https://github.com/maaaaz/dotfiles/blob/master/kali_missing_packages.txt
  - Microsoft Sysmon and ProcDump for Linux
- Bash as default shell
- A friendlier [`.vimrc`](https://github.com/maaaaz/dotfiles/blob/master/.vimrc) in the `root` and `kali` homes
- VMWare and VirtualBox compatibility
- Virtualbox permission fix by adding the `kali` to the `vboxsf` group
- A Python `venvcommon` virtualenv (in the `root` home, use `workon venvcommon`), containing [common infosec Python packages](https://github.com/maaaaz/dotfiles/blob/master/python_common.txt)
- azerty keymap and France timezone (sorry, I am french), but you can easily change these settings after

Releases
---------
- See https://github.com/maaaaz/Kalicustom/releases
- Releases are hosted on `archive.org` because:
  - `archive.org` accept larger files than Github release feature (2 GB, which is not enough)
  - `archive.org` provide multiple downloading capacities: direct download, torrent etc.
  - `archive.org` is an awesome project
- Release file are 7 GB compressed | 25 GB decompressed

Changelog
---------
2024-04-20: first release

Copyright and license
---------------------
* All trademarks, service marks, trade names and product names appearing on this repository are the property of their respective owners 
