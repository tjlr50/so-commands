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
