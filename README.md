# Javier_Ezpeleta_auditori_SEAS

## 1. Configuración de Red y Conectividad
Se han configurado dos máquinas Ubuntu con una red interna.
- IP Atacante: 192.168.100.10
- IP Objetivo: 192.168.100.20

> **Captura de Ping:**
> ![Ping](<img width="896" height="459" alt="Captura de pantalla 2026-04-09 103409" src="https://github.com/user-attachments/assets/7c76f629-5f2f-4d3b-b71f-07b83550ccb7" />
)

## 2. Escaneo de Puertos (Nmap)
Se realiza un escaneo para detectar los servicios SSH (2222) y FTP (4321).
`nmap -sV -p 2222,4321 192.168.100.20`

> **Captura de Nmap:**
> ![Nmap](<img width="1282" height="881" alt="Captura de pantalla 2026-04-09 103502" src="https://github.com/user-attachments/assets/d4fdd8c7-6f51-41a1-9a12-d440b5cce34e" />
)

## 3. Servidor FTP Anónimo
Configurado en el puerto 4321. Se accede para recuperar el archivo de flag.

> **Captura de acceso FTP:**
> ![FTP](<img width="1279" height="884" alt="Captura de pantalla 2026-04-09 104421" src="https://github.com/user-attachments/assets/00eebdeb-8312-4b21-b828-d79137f9a0b7" />
)

## 4. Ataque de Fuerza Bruta (Hydra)
Se utiliza Hydra con un diccionario personalizado para obtener la contraseña del usuario.
`hydra -l hola -P pass.txt ssh://192.168.100.20:2222`

> **Captura de Hydra:**
> ![Hydra](<img width="1280" height="884" alt="Captura de pantalla 2026-04-09 105319" src="https://github.com/user-attachments/assets/d5ee4115-d8ee-4e8c-95fd-650791a07c19" />
)

## 5. Acceso SSH por Clave Pública
Se generan claves con `ssh-keygen` y se transfieren con `ssh-copy-id`.

> **Captura de acceso sin contraseña:**
> ![SSH-Key](<img width="1210" height="709" alt="Captura de pantalla 2026-04-09 105828" src="https://github.com/user-attachments/assets/e96de42e-1c82-4acd-8a9a-897632db8737" />)
