# Ubuntu development machine

```
# You have to copy, paste, and press enter on each line, sometimes it needs credentials.
# TODO: Automate!
sudo apt-get update
sudo apt-get install docker
sudo apt-get install docker-compose
sudo snap install --classic code # Command to open directory/file in VSCode.

git config --global user.name <NAME>
git config --global user.email <GITHUB-USERNAME>@users.noreply.github.com

# Github.
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-key C99B11DEB97541F0
sudo apt-add-repository https://cli.github.com/packages
sudo apt update
sudo apt install gh
gh auth login
# Choose SSH.

ssh-keygen
cat ~/.ssh/id_rsa.pub
# Add ssh key to Github: https://github.com/settings/ssh/new

# Heroku.
sudo snap install --classic heroku
heroku login -i
```

# Help
```
docker info # Check for docker errors
sudo chown -R $USER:$USER . # Change ownership of all files and folders here and below
sudo chown $USER /var/run/docker.sock # Fix docker permission error
sudo dockerd &> /dev/null & # Start docker daemon if it crashes.
heroku apps -A # List all Heroku apps
heroku ps:exec -a <APP_NAME> # SSH to app
sudo apt update && sudo apt upgrade # Upgrade packages
```

