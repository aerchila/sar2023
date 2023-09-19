#Tema: Sflow
### Instrucciones :
Primeo haremos la instalación y nos vamos a adentrar en la plataforma para usar sFlow-rt y luego el laboratorio con una de las aplicaciones que trae la plataforma. 
### Lista de comandos.
1. Descargamos de la web el github donde obtenemos ``` hsdlowd ``` el cual actiba el protocolo ``` sflow ``` en ubuntu
    ```
   wget https://github.com/sflow/host-sflow/releases/download/v2.0.25-3/hsflowd-ubuntu18_2.0.25-3_amd64.deb
   ```
2. Instalamos con ``` sudo dpkg -i ``` el cual se utiliza para instalar paquetes Debian.
   ``` sudo ```: Este prefijo se utiliza para ejecutar el comando con privilegios de superusuario
   ``` dpkg ```: Este es el comando principal que se utiliza para gestionar paquetes en sistemas basados en Debian
   ```-i ```: Esta opción le indica a dpkg que debe instalar un paquete. 
    ```
   sudo dpkg -i hsflowd-ubuntu18_2.0.25-3_amd64.deb
   ```
