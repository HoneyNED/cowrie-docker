# cowrie-docker
A dockerized cowrie

## Installation
Run `docker-compose build` which will create a docker image based on Ubuntu 16.04 LTS with cowrie installed. Afterwards, edit the default cowrie configuration file in `etc/cowrie.cfg` and edit the sensorname and hostname. Now edit the `.env` file and add the IP-address of your Splunk server where we should forward all cowrie events to.

You also want to give the Docker container full access to the directories `dl`, `etc` and `log` by running this command: `chmod -R 777 dl etc log`.

Now run the container with `docker-compose up` and see if it works. Run this command with `-d` to run it in the background.

You can connect to the honeypot using `ssh localhost -p 2222 -l root`.
