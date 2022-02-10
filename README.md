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
