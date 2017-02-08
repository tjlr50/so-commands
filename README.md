# Comandos CentOS 7

## Resetear password

En el menú de boot presionar la tecla `e`  
Cambiar `ro` por `rw init=/sysroot/bin/sh`
Presionar `ctrl+x`  
Ejecutar los siguientes comandos
```
#chroot /sysroot
#passwd root
#touch /.autorelabel
#exit
#reboot
```
## Comandos comunes

| Comando   | Descripción   |
|---|---|
| ip addr | |
| ip route show | |
| ifdown ens33 | Desactivar interfaz de red |
| ifup ens33 | Activar interfaz de red |
| systemctl restart network.service | Reiniciar las interfaces de red |
| systemctl status network.service | Obtener el estado de las interfaces de red |
| ssh root@192.168.10.128 | Realizar una conexión remota |
| yum install httpd -y | |
| firewall-cmd --get-active-zones | |
| firewall-cmd --zone=public --add-port=80/tcp --permanent | |
| firewall-cmd --reload | |
| systemctl enable httpd |  |
| systemctl is-enabled httpd | |
| systemctl start httpd |  |
| systemctl status httpd |  |
| systemctl list-unit-files --type=service | |

| Comando   | Descripción   |
|---|---|
| nmcli -p dev | Listar conexiones de red y estado |
| nmcli con up ens33 | |
| nmcli con down ens33 | |
| ip route add 10.10.20.0/24 via 192.168.50.100 dev eth0 | |
| ip addr add 192.168.50.5/24 dev eth1 | | 
| ip addr del 192.168.50.5/24 dev eth1 | |  

# Archivos configuración

/etc/sysconfig/network-scripts/ifcfg-ens34
```
HWADDR=00:08:A2:0A:BA:B8
TYPE=Ethernet
BOOTPROTO=none
IPADDR=192.168.130.2
PREFIX=24
GATEWAY=192.168.130.1
DNS1=8.8.8.8
IPV4_FAILURE_FATAL=no
IPV6INIT=no
NAME=ens34
# This is system specific and can be created using 'uuidgen ens34' command #
UUID=41171a6f-bce1-44de-8a6e-cf5e782f8bd6
DEVICE=ens34
ONBOOT=yes
```
# Comandos CentOS 6

| Comando   | Descripción   |
|---|---|
| service --status-all | Listar servicios |
| chkconfig --list | Listar servicios y runlevels |

