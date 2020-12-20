# deployer-box
Vagrant box for deployphp/deployer with additional functions and API

# Installation
## Windows 10:
1. Install PHP cli if not installed
2. Install composer if not installed
3. Install VirtualBox and VirtualBox ext pack
4. Install Vagrant
5. Install git
6. Create folder in your home directory (In my example it "deployment") and go inside
7. Run git clone https://github.com/asafov/deployer-box.git deployment
8. Go to folder deployment
9. Rename Homestead.yaml.example to Homestead.yaml and edit it:
   9.1. Replace ~/.ssh/id_rsa.pub to path for your ssh pub key
   9.2. Replace ~/.ssh/id_rsa to path for your ssh private key
   9.3. Replace C:\Users\i\ to your user home directory
   9.4. Full configuration manual is here: https://laravel.com/docs/8.x/homestead
10. Run "vagrant box add laravel/homestead"
11. Edit your hosts file - add record for deployer.local
12. Run composer install
13. Run "vagrant up" and wait for installation complete
14. Connect by SSH to your box: ssh 127.0.0.1 at port 2222