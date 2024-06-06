# AdGuarHome

apt install aptitude docker.io lm-sensors snmpd chrony

docker pull adguard/adguardhome

mkdir -p /home/docker/volumes/adguard/conf /home/docker/volumes/adguard/work

docker run -d --name adguardhome --restart unless-stopped -v /home/docker/volumes/adguard/conf:/opt/adguardhome/conf -v /home/docker/volumes/adguard/work:/opt/adguardhome/work --network host adguard/adguardhome
