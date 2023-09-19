#Laboratorio sFlow
### Intrucciones: 
Solo necesitaran su ubuntu server.
### Lista de comandos.
1. Actualizar antes de iniciar 
```
   sudo apt update
   ```
2. Buscar entre todas las aplicaciones la de Mininet e instalar. 
   ![Aplicaciones](https://github.com/aerchila/sar2023/blob/main/apps.png)
   ```
   sudo apt install mininet
   ```
   ```
   sudo /usr/local/sflow-rt/get-app.sh sflow-rt mininet-dashboard
   ```
3. Ir a un navegador y colocar ```IP_SERVER:8008```
4. Moverse a la carpeta ```sflow-rt```
   ```
   cd sflow-rt
   ```
   **Si en caso no funcionara, realizar estos dos pasos más**
   ```
   wget https://inmon.com/products/sFlow-RT/sflow-rt.tar.gz
   ```
   
   ```
   tar -xvzf sflow-rt.tar.gz
   ```
   **De caso contrario seguir con lo demas.**
5. Correr el comando
   ```
   sudo mn --custom extras/sflow.py --link tc,bw=10 --topo tree,depth=2,fanout=2 --test iperf
   ```
   **Dentro de la carpeta ```sflow-rt```**
6. Ir al navegador, y en la pestaña apps seleccionar mininet
   ![Aplicaciones](https://github.com/aerchila/sar2023/blob/main/apps.png)
