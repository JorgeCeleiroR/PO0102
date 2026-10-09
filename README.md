# Práctica Cockpit

Comprobación de la IP

<img width="807" height="613" alt="image" src="https://github.com/user-attachments/assets/d6f1abae-4461-4b2b-a0c6-036f92781f4e" />



Script de instalación

Lo he hecho sin .env. He creado la carpeta scripts y dentro el script cockpit-install.sh.


mkdir /scripts
cd /scripts


Código del script:


#!/bin/bash
set -e

echo "=== 1. ACTUALIZANDO SISTEMA ==="
sudo apt update

echo "=== 2. INSTALANDO COCKPIT ==="
sudo apt install -y cockpit

echo "=== 3. CORTAFUEGOS ==="
sudo ufw allow 22/tcp
sudo ufw allow 9090/tcp
sudo ufw --force enable

echo "¡PROCESO COMPLETADO!"
echo "Accede en: https://192.168.100.10:9090"


Ejecutar el script


sudo chmod +x cockpit-install.sh
./cockpit-install.sh




Comprobante de Cockpit

<img width="1917" height="947" alt="image" src="https://github.com/user-attachments/assets/480fa468-1ca3-43e1-b5f2-9c68bb84365e" />
