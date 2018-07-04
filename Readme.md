# My fedora workstation setup

tired to re-install evrything each time i change/reinstall my computer. So i wrote a simple anible playbook in order to set it up.

## which linux ?
Fedora only (lol)

## setup
on a fresh fedora installation, install ansible from github

~~~
cd /usr/local/src
git clone https://github.com/ansible/ansible.git
cd ./ansible
git checkout stable-2.6 # <-- take the latest stable
~~~

install packaging lib from pip
~~~
cd /usr/local/src
pip install packaging
~~~

install ansible
~~~
cd /usr/local/src
pip install -r requirements.txt
make
make install
~~~

clone this project and run ansible
~~~
git clone https://github.com/lapinferoce/ansible-fedora-self.git ./this-computer
cd ./this-computer
ansible-playbook -K ./playbook.yml
~~~

