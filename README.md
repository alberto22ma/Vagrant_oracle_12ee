# Oracle 12c en Linux con Vagrant

Archivos de configuración para una máquina virtual con Oracle Database 12.1.0.2 en Linux CentOS 6.5 (64 bits) usando sólo Vagrant y los dos ficheros de instalación de la base de datos.

## Inicio rápido

1. Descargar e instalar [VirtualBox][2] y sus extensiones cuando lo pida.
2. Descargar e instalar [Vagrant][1].
3. Clonar [este repositorio][3] de GitHub en una carpeta del ordenador.
4. Descargar los archivos zip de instalación desde [oracle][4]:

	- linuxamd64_12c_database_1of2.zip 
	- linuxamd64_12c_database_2of2.zip
	
* Requiere registrarse y aceptar el acuerdo de licencia

5. Mover los dos archivos zip descargados en la carpeta [oracle12ee](./oracle12ee/), sin descomprimir ni crear ningún subdirectorio adicional.
6. Ejecutamo el siguiente comando `vagrant up` en la carpeta que contiene el Vagrantfile.

El proceso de instalación durará entre 20 y 30 minutos.

## Datos de acceso a la máquina virtual

- Dirección IP: `10.10.10.9`.
- La contraseña de `sys` y `system` es `oracle`.
- Los usuarios del sistema operativo `root` y `vagrant` tienen como contraseña `vagrant`. El usuario `oracle` tiene `oracle` como contraseña.
- El SID de la base de datos es `db12102`.
- En la máquina virtual la carpeta `/vagrant` corresponde a la carpeta donde tengamos el Vagrantfile.
- La base de datos esta escuchando en el puerto por defecto, el 1521.

## Comandos básicos de Vagrant

### Arrancar el servidor
```bash
vagrant up
```

### Pausar el servidor
```bash
vagrant suspend
```

### Apagar el servidor
```bash
vagrant halt
```

### Borrar el servidor ⚠
```bash
vagrant destroy
```

### Acceder por SSH al servidor
```bash
vagrant ssh
```
*En Windows hay que tener un cliente SSH para que este comando funcione. Se puede instalar el cliente de [Git][6] y utilizar el shell que proporciona, que incluye SSH.

[1]: https://www.vagrantup.com/downloads.html
[2]: https://www.virtualbox.org/wiki/Downloads
[3]: https://github.com/alberto22ma/Vagrant_oracle_12ee.git
[4]: https://www.oracle.com/technetwork/database/enterprise-edition/downloads/database12c-linux-download-2240591.html
[5]: http://nunki.diocesanas.org/software/oracle12ee/
[6]: https://git-scm.com/downloads
