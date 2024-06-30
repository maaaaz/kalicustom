#!/bin/sh

chsh --shell /usr/bin/bash kali
chsh --shell /usr/bin/bash root

wget -nv "https://github.com/maaaaz/dotfiles/raw/master/.vimrc" -O "/root/.vimrc"
su kali -c "wget -nv 'https://github.com/maaaaz/dotfiles/raw/master/.vimrc' -O '/home/kali/.vimrc'"

rm -rf /etc/localtime
ln -s /usr/share/zoneinfo/Europe/Paris /etc/localtime
sh -c "sed -i 's/XKBLAYOUT=\"\w*\"/XKBLAYOUT=\"'fr'\"/g' /etc/default/keyboard"

wget -nv 'https://packages.microsoft.com/debian/12/prod/pool/main/s/sysinternalsebpf/sysinternalsebpf_1.3.0_amd64.deb' -O '/tmp/sysinternalsebpf_1.3.0_amd64.deb'
dpkg -i '/tmp/sysinternalsebpf_1.3.0_amd64.deb'

wget -nv 'https://packages.microsoft.com/debian/12/prod/pool/main/s/sysmonforlinux/sysmonforlinux_1.3.2_amd64.deb' -O '/tmp/sysmonforlinux_1.3.2_amd64.deb'
dpkg -i '/tmp/sysmonforlinux_1.3.2_amd64.deb'

wget -nv 'https://packages.microsoft.com/debian/12/prod/pool/main/p/procdump/procdump_3.2.0_amd64.deb' -O '/tmp/procdump_3.2.0_amd64.deb'
dpkg -i '/tmp/procdump_3.2.0_amd64.deb' 

mkdir -p /opt/escobar/
wget -nv 'https://github.com/savely-krasovsky/escobar/releases/download/v3.0.1/escobar-3.0.1-linux-amd64.tar.gz' -O '/opt/escobar/escobar-3.0.1-linux-amd64.tar.gz'
tar -xvf '/opt/escobar/escobar-3.0.1-linux-amd64.tar.gz' --directory '/opt/escobar/'

venv_home="grep -i 'workon_home' ~/.bashrc ||  echo 'export WORKON_HOME=~/.virtualenvs' >> ~/.bashrc"
venv_python="grep -i 'virtualenvwrapper_python' ~/.bashrc || echo 'export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3' >> ~/.bashrc"
venv_wrapper="grep -i 'virtualenvwrapper.sh' ~/.bashrc ||  echo 'source /usr/share/virtualenvwrapper/virtualenvwrapper.sh' >> ~/.bashrc"

su root -c "($venv_home) && ($venv_python) && ($venv_wrapper)"
su kali -c "($venv_home) && ($venv_python) && ($venv_wrapper)"

bash -c "WORKON_HOME=~/.virtualenvs VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3 && source /usr/share/virtualenvwrapper/virtualenvwrapper.sh && mkvirtualenv -p python3 venvcommon && workon venvcommon && wget -nv 'https://github.com/maaaaz/dotfiles/raw/master/python_common.txt' -O '/tmp/python_common.txt' && pip3 install -r '/tmp/python_common.txt'"
