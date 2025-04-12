# AdGuardHome-Raspbian

`apt install aptitude chrony curl dnsutils docker.io iperf3 lm-sensors net-tools rsyslog snmpd wavemon`

`mkdir -p /home/docker/adguardhome/vol/conf /home/docker/adguardhome/vol/work`

```
docker run -d --name adguardhome --restart unless-stopped --network host \
  -v /home/docker/adguardhome/vol/conf:/opt/adguardhome/conf \
  -v /home/docker/adguardhome/vol/work:/opt/adguardhome/work \
  adguard/adguardhome
```
