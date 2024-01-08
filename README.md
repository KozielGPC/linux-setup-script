# linux-setup-script
Shell script to install most used packages and applications for development

Installed applications:
* Node
* VSCode
  *   Extentions: ESLint, GitLens, Prettier, Codeium, Jest Runner

* Git
* ZSH and OhMyZSH
* MongoDB
* MongoDB Compass
* Dbeaver
* Insomnia
* Docker
* Docker Compose
* Another Redis Desktop Manager
* Minikube

## Installation
* Clone the `script.sh` file
* Set execution access with `chmod +x script.sh`
* Run `./script.sh`

## Export envinronment variables permanently
To export envinronment variables permanently you can add the following code to the script:

```shell
echo "Enter variable name: "
read variable_name
echo "Enter variable value: "
read variable_value
echo "adding " $variable_name " to environment variables: " $variable_value
echo "export "$variable_name"="$variable_value>>~/.bashrc
echo $variable_name"="$variable_value>>~/.profile
echo $variable_name"="$variable_value>>/etc/environment
source ~/.bashrc
source ~/.profile
echo "do you want to restart your computer to apply changes in /etc/environment file? yes(y)no(n)"
read restart
case $restart in
    y) sudo shutdown -r 0;;
    n) echo "don't forget to restart your computer manually";;
esac
exit
```
* Note: make sure you run the script with *sudo*
