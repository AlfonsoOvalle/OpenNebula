# Instalación OpenNebula miniOne[Parámetros de instalación](#Parámetros) [![N|Solid](https://opennebula.io/wp-content/uploads/2019/04/img-logo-blue.svg)](https://docs.opennebula.io/minione/)

Actualizamos los repositorios
```sh
apt-get update
```
Descargamos el bash de miniOne
```sh
wget 'https://github.com/OpenNebula/minione/releases/latest/download/minione'
```

Concedemos permisos al script
```sh
chmod 777 minione
```
**Si se trabaja sobre una instalación mínima de Ubuntu, se deben instalar las siguientes herramientas:**
```sh
sudo apt install curl -y
sudo apt-get install augeas-tools -y
sudo apt-get install openssh-server -y
```

Para realizar una instalación detallada se hace uso del parámetro --verbose, este instalara un hipervisor KVM por defecto

```sh
sudo bash minione --verbose
```
Si se desea instalar un hipervisor LXD
```sh
sudo bash minione --verbose --lxd
```
Algunos parámetros que se pueden utilizar  [Parámetros de instalación](####Parámetros)


 
# Parámetros

| Parámetro | Descripción |
| ------ | ------ |
|--help	| Mostrar todos los modificadores de línea de comando disponibles.|
|--verbose |	Registro detallado.|
|--lxd|	Implemente el entorno para evaluar el hipervisor LXD.|
|--version|	Especifique una versión particular de OpenNebula para implementar|
|--frontend |Solo frontend. Omitir hipervisor / red. Configuración.|
|--sunstone-port|	Puerto para enlazar la interfaz de usuario web de Sunstone|
|--password |	Contraseña inicial para un usuario dedicado de oneadmin|
|--vm-password |	Contraseña para iniciar sesión en máquinas vrtuales a través de VNC integrado|
|--purge | Desinstale OpenNebula y elimine todos los rastros.|
