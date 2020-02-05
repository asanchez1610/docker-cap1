Proceso de Pre-Instalación
============================

Vamos a trabjar con Centos 7.x para lo cual, lo primero que debemos hacer es siempre actualizar el OS para ello realizamos las sgts acciones: 

> yum -y install epel-release

> yum update -y

> yum -y install vim vim-enhanced

Desactivamos SELinux: 

> vim /etc/selinux/config 

Aqui cambiamos le valor de "enforcing" por "disabled" 

Por ultimo : 

> reboot 

Proceso de Post-Instalación
============================

Para este punto, la distribución linux donde realizamos la instalcion es Centos, pero puede ser en cualquier distribucion linux, por lo cual este procedimiento de instalación es generico:

> curl -fsSL https://get.docker.com -o get-docker.sh

> sh get-docker.sh

Ahora vamos a dejar activo el servicio por defecto y lo inicializamos

> systemctl enable docker 

> systemctl start docker

* Debemos crear un usuario que sea dueño del proceso ( docker ) por temas de seguridad. Tal y como indica la recomendación de docker post instalacion.
