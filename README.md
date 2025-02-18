# H.D.O
repertorio para la clase de Habilidades DevOps 2025
mkdir clonar_repo.sh
#!/bin/bash

CARPETA="/var/www/html/mi_proyecto"  
REPO_URL="https://github.com/usuario/repositorio.git"  

echo "Creando carpeta en $CARPETA..."
sudo mkdir -p "$CARPETA"
sudo chown -R $USER:$USER "$CARPETA" 

echo "Clonando el repositorio..."
cd "$CARPETA" || { echo "Error al acceder a la carpeta"; exit 1; }
git clone "$REPO_URL" .

echo "Listo! El repositorio se clonó en $(pwd)"
