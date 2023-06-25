# aleocpu
aleocpu
sudo apt update && sudo apt upgrade -y

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y

source $HOME/.cargo/env

apt install ufw -y 
ufw allow ssh 
ufw allow https 
ufw allow http 
ufw allow 4133
ufw allow 3033
ufw enable

sudo apt install screen -y

git clone https://github.com/AleoHQ/snarkOS.git --depth 1

cd snarkOS

./build_ubuntu.sh

cargo install --path .

screen -S client

./run-client.sh

\\\\\\\\\\Press CTRL+A+D

snarkos account new

\\\\\\\\\\\\Private Key  APrivateKey1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
   \\\\\\\\\\  View Key  AViewKey1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
 \\\\\\\\    Address  aleo1xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

screen -S prover

./run-prover.sh

\\\\\\Enter your private Key

\\\\ Press CTRL+A+D

go to site https://www.aleo.network/transactions



