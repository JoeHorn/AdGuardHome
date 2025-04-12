# AdGuardHome-Raspbian

`apt install aptitude chrony curl dnsutils docker.io iperf3 lm-sensors net-tools rsync rsyslog snmpd wavemon`

`mkdir -p /home/docker/adguardhome/conf /home/docker/adguardhome/work`

```
docker run -d --name adguardhome --restart unless-stopped --network host \
  -v /home/docker/adguardhome/conf:/opt/adguardhome/conf \
  -v /home/docker/adguardhome/work:/opt/adguardhome/work \
  adguard/adguardhome
```
