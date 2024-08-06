# Warden Magento Installer
Creates a Magento 2 installation automatically with ✨Warden✨

## Install

- You must first install warden https://docs.warden.dev/installing.html
- Create a directory
- Copy the installmagento python script to this directory

## Pre use

- the warden container must be running, so run **warden svc up**

## How to use

- ./installmagento -d domain -v magento-version

    Example: ./installmagento -d test2.4.4 -v 2.4.4

- Optional arguments:

    -v magento_version : installs the magento version given 

    -s : Will install magento with the sampledata module

    -n ngrok-token : Will setup ngrok for the magento installation, the ngrok url will be printed at the end

    -r : removes ngrok and sets the default url

- Once the script ends your magento url will be https://app.domain.test (If you didn't use the ngrok argument), On Ubuntu follow this: https://docs.warden.dev/configuration/dns-resolver.html#systemd-resolved
- It should work on macOS, can't test it properly right now
- The admin page is /demoadmin (You can edit default values on top of the script)

## TO-DO

    - Nothing, the script is perfect already
    - Install opayo automatically with the -o argument
    - Install mailchimp automatically with the -m argument


Based on https://github.com/gonzaloebiz/wardenscripts
