#setup
sudo apt install npm 
sudo apt update
sudo apt -y install curl dirmngr apt-transport-https lsb-release ca-certificates
curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
sudo apt -y install nodejs

sudo apt-get update
sudo apt-get upgrade

sudo npm install --global yarn

sudo npm install -g @angular/cli
cd paperless-ng/src-ui
npm install

#create image
docker build . -t paperless
cd docker/compose/
docker-compose up -d