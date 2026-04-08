# Javier_Ezpeleta_auditori_SEAS

## 1. Configuración de Red y Conectividad
Se han configurado dos máquinas Ubuntu con una red interna.
- IP Atacante: 192.168.100.10
- IP Objetivo: 192.168.100.20

> **Captura de Ping:**
> ![Ping](nombre_de_tu_foto_ping.png)

## 2. Escaneo de Puertos (Nmap)
Se realiza un escaneo para detectar los servicios SSH (2222) y FTP (4321).
`nmap -sV -p 2222,4321 192.168.100.20`

> **Captura de Nmap:**
> ![Nmap](nombre_de_tu_foto_nmap.png)

## 3. Servidor FTP Anónimo
Configurado en el puerto 4321. Se accede para recuperar el archivo de flag.

> **Captura de acceso FTP:**
> ![FTP](nombre_de_tu_foto_ftp.png)

## 4. Ataque de Fuerza Bruta (Hydra)
Se utiliza Hydra con un diccionario personalizado para obtener la contraseña del usuario.
`hydra -l hola -P pass.txt ssh://192.168.100.20:2222`

> **Captura de Hydra:**
> ![Hydra](nombre_de_tu_foto_hydra.png)

## 5. Acceso SSH por Clave Pública
Se generan claves con `ssh-keygen` y se transfieren con `ssh-copy-id`.

> **Captura de acceso sin contraseña:**
> ![SSH-Key](nombre_de_tu_foto_ssh.png)
