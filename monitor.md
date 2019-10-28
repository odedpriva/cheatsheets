# monitoring

## findout the server ip and AWS instance name

```bash

```

## login to server

```bash
ssh ec2-user@172.31.151.246@production-eu-west-1@production-eu-west-1.luminate.luminatesite.com -i ~/.ssh/luminate
```

## dmesg

```bash
dmesg  --ctime --syslog  --nopager | less
```

## journalctl

```bash
journalctl --since "2019-10-10 6:50:00" --until "2019-10-10 7:10:00" --identifier docker --identifier kubelet --identifier dhclient
```

