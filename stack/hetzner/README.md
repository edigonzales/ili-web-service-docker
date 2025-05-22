# Hetzner

## Server erstellen

- Standort: Falkenstein
- Image: Apps - Docker CE
- Typ: CAX11 (ARM)
- Networking: Öffentliche IPv4 und IPv6.
- SSH-Keys: alle benötigten
- Firewalls: todo
- Backup: todo
- Cloud config:

```
#cloud-config
users:
  - name: iliws
    shell: /bin/bash
    groups: docker

package_upgrade: false

runcmd:
  - [su, iliws, -c, "git clone https://github.com/edigonzales/ili-web-service-docker.git /home/iliws/ili-web-service-docker"]
```

- Anwendung starten: todo (siehe unten)
- Floating IP: https://docs.hetzner.com/de/cloud/floating-ips/persistent-configuration/ -> todo: in cloud-config (chmod 700 /etc/netplan/60-floating-ip.yaml)

## Anwendung deployen

```
ssh root@xxxxxxxxxx
```

```
sudo su iliws
```

```
cd && git clone https://github.com/edigonzales/ili-web-service-docker.git 
```

```
docker compose -f ili-web-service-docker/stack/hetzner/docker-compose.yml -p ili-web-service up
```
