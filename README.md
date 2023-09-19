# Tema: Sflow
### Instrucciones :
Primeo haremos la instalación y nos vamos a adentrar en la plataforma para usar sFlow-rt y luego el laboratorio con una de las aplicaciones que trae la plataforma. 
### Lista de comandos.
1. Descargamos de la web el github donde obtenemos ``` hsdlowd ``` el cual activa el protocolo ``` sflow ``` en ubuntu
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
3. Habilitar el protocolo en ubuntu
   ```
   sudo systemctl enable hsflowd
   ```
4. Instalar java para que se puede ejecutar
    ```
   sudo apt install openjdk-11-jre-headless
   ```
5. Actualizar, esto para que actualice cualquier paquete que haya encontrado una version anterior
   ```
   sudo apt update
   ```
6. Instalar el entorno de ejecución de Java
    ```
   sudo apt install default-jre
   ```
7. Descargamos sFlow
   ```
   wget https://inmon.com/products/sFlow-RT/sflow-rt_3.0-1673.deb
   ```
8. Instalamos lo que descargamos
    ```
   sudo dpkg -i sflow-rt_3.0-1673.deb
   ```
9. habilitamos sFlow-rt con ``` enable ``` 
    ```
   sudo systemctl enable sflow-rt
   ```
    Inicializamos con ``` start ```
    ```
   sudo systemctl start sflow-rt
   ```
    y verificamos si esta funcionando con ``` status ```
    ```
   sudo systemctl status sflow-rt
   ```

    
10. Este comando sirve para instalar en la plataforma opciones y configuraciones en el dashboard principal
```
   LATEST=`wget -qO - https://inmon.com/products/sFlow-RT/latest.txt`
   ```
```
   wget https://inmon.com/products/sFlow-RT/sflow-rt_$LATEST.deb
   ```

11. Instalar lo descargado
```
   sudo dpkg -i sflow-rt_$LATEST.deb
   ```
    
12. Habilitar el puerto con ``` sudo ufw allow ```, esto para permitir el tráfico entrante de una aplicación o puerto específico
```
   sudo ufw allow 8008/tcp
   ```
    
12.1. **Si en caso el comando no funciona correr ``` sudo systemctl start ufw ```, para activar ufw (Uncomplicated Firewall)**
```
   sudo systemctl start ufw
   ```

13. Entrar a un sitio web y colocar la ip seguido :8008 ej. ``` IP_SERVER:8008 ≈ 192.168.79.131:8008 ```
