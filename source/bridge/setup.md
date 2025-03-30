# Setting Up your Bridge Bot

This guide will help you set up your bridge bot for the first time, as well as update it in the future.

## Prerequisites

- You have made a [Discord bot](https://discord.com/developers/applications) and have the token.
- You have a Minecraft account in a guild on Hypixel

Please note that this setup guide was made for Linux/Ubuntu machines.

## Initial Setup

```shell
# Ensure we are in the home directory
cd ~

# Install nvm & node

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash
source ~/.bashrc
nvm install 19.7.0

# Install pm2 for process management
npm install -g pm2

# Install python3
sudo apt-get update
sudo apt install python3-pip
apt install python3.12-venv

# Clone the project
git clone https://github.com/Jacktheguys/GuildBridgeBot

# Create directories for bridge bots
mkdir bridges

# Create config file
mv GuildBridgeBot/example.config.json GuildBridgeBot/config.json
```


## Creating A New Bridge Bot

```shell
# Ensure we are in the home directory
cd ~

# Copy files for a new bridge bot
mkdir bridges/<NAME_OF_GUILD>
cp -r GuildBridgeBot/* bridges/<NAME_OF_GUILD>/
cd bridges/<NAME_OF_GUILD>

# Create a virtal environment
python3 -m venv venv
source venv/bin/activate

# Install requirements
python3 -m pip install -U -r requirements.txt

# Update the config
nano config.json

# Then run the bot with pm2
pm2 start main.py --name <NAME_OF_GUILD>-BridgeBot --interpreter ./venv/bin/python --restart-delay=3000

# To actually start the bot, you will need to log in with Microsoft.
# To do this, run the following command and follow the instructions:
pm2 logs <NAME_OF_GUILD>-BridgeBot
```

## Updating A Bridge Bot

Run the `!update` command in Discord, or, use the following commands in your bridge bot's directory:

```shell
# Update files
./venv/bin/python main.py update

# Restart the bot
# If you do not know what the process name is, you can get it with `pm2 ls`
pm2 restart <process-name>
```
