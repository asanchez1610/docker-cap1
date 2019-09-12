# Proceso de instalación

Para este punto, la distribución linux es "agnostica" por lo cual este procedimiento es generico:

> curl -fsSL https://get.docker.com -o get-docker.sh

> sh get-docker.sh

#### Observacion
En el caso de RHEL/Centos debemos deshabilitar Selinux y Firewalld

Posterior a la instalación, ejecutamos:

systemctl enable docker && systemctl start docker

#### Observacion
Debemos crear un usuario que sea dueño del proceso ( docker ) por temas de seguridad.
Tal y como indica la recomendación de docker post instalacion
