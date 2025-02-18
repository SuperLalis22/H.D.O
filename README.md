# H.D.O
repertorio para la clase de Habilidades DevOps 2025
mkdir clonar_repo.sh
#!/bin/bash

# Configuración
CARPETA="/var/www/html/mi_proyecto"  # Ruta donde se clonará el repo
REPO_URL="https://github.com/usuario/repositorio.git"  # URL del repo a clonar

echo "Creando carpeta en $CARPETA..."
sudo mkdir -p "$CARPETA"
sudo chown -R $USER:$USER "$CARPETA"  # Damos permisos al usuario actual

echo "Clonando el repositorio..."
cd "$CARPETA" || { echo "Error al acceder a la carpeta"; exit 1; }
git clone "$REPO_URL" .

echo "Listo! El repositorio se clonó en $(pwd)"
