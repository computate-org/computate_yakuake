# Install yakuake

## Install the latest Python and setup a new Python virtualenv

```bash
sudo yum install -y git python3 python3-pip python3-virtualenv python3-libselinux python3-libsemanage python3-policycoreutils
virtualenv-3 ~/python
source ~/python/bin/activate
echo "source ~/python/bin/activate" | tee -a ~/.bashrc
```

## Install the latest Ansible

```bash
pip install setuptools_rust wheel
pip install --upgrade pip
pip install ansible selinux setools
```

## Install the yakuake ansible role

### Create a directory for the ansible role. 

```bash
install -d ~/.ansible/roles/computate.computate_yakuake
```

### Clone the yakuake ansible role. 

```bash
git clone git@github.com:computate-org/computate_yakuake.git ~/.ansible/roles/computate.computate_yakuake
```

## Run the yakuake ansible playbook to install the application locally (requires sudo privileges with -K). 

```bash
cd ~/.ansible/roles/computate.computate_yakuake
ansible-playbook -K install.yml
```



