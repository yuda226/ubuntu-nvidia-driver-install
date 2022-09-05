# ubuntu-nvidia-driver-install

Install nvidia driver on ubuntu steps

## Reference
[linuxbabe.com](https://www.linuxbabe.com/ubuntu/install-nvidia-driver-ubuntu-18-04)
[linuxconfig.org](https://linuxconfig.org/how-to-install-the-nvidia-drivers-on-ubuntu-18-04-bionic)

## Steps

```bash
# Add repository and update
sudo add-apt-repository ppa:graphics-drivers/ppa
sudo apt update

# Find recommended driver for GPU
ubuntu-drivers devices

#Auto install or install with specific driver
sudo ubuntu-drivers autoinstall
OR
sudo apt install nvidia-driver-$VersionNumber

#Debug, sometimes might encouter dependency problems, shall stop installing and upgrade
sudo apt update && sudo apt upgrade
sudo ubuntu-drivers autoinstall

# Reboot system and driver validating 
reboot 
THEN
nvidia-smi
```

# dpkg: error processing package python

accidently removed python-pkg
## Reference
https://stackoverflow.com/questions/43064696/how-to-restore-after-accidentally-apt-get-remove-python

## Steps

```bash
# Install python/python3
sudo apt-get install --reinstall python python-chardet python-colorama python-distlib python-django python-django-tables2 python-six python-html5lib python-lxml python-minimal python-pkg-resources python-setuptools python-urllib3 python-requests python-pip python-virtualenv

sudo apt-get install --reinstall python-dnspython

sudo apt autoremove

sudo apt-get -f install

# Install gnome 
## try this first if above not working 
sudo apt install gnome

#Install ubuntu-desktop if GUI not working
sudo apt-get install --reinstall ubuntu-desktop

```

