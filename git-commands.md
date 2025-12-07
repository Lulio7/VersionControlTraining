# 📘 GIT-COMMANDS.md  
Comandos básicos de Git para trabajar con proyectos PBIP + Power BI

## 🧭 Configuración inicial
``bash
Configurar usuario: 
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"

Ver configuración actual: 
git config --list

## 📥 Clonar un repositorio: 
git clone https://github.com/usuario/repositorio.git

## 🌿 Ramas

Ver ramas existentes: 
git branch

Crear nueva rama: 
git checkout -b nombre-de-rama

Cambiar de rama: 
git checkout main

Eliminar una rama local: 
git branch -d nombre-de-rama

Eliminar rama remota: 
git push origin --delete nombre-de-rama

## 📌 Estado y seguimiento

Ver cambios pendientes: 
git status

Ver diferencias en archivos: 
git diff

## ➕ Añadir archivos al commit

Añadir un archivo específico: 
git add archivo

Añadir todo: 
git add .

## 💾 Commits

Crear un commit: 
git commit -m "Descripción del cambio"

Modificar el último commit (sin cambiar contenido): 
git commit --amend -m "Nuevo mensaje"

## 🚀 Subir cambios (Push)

git push origin nombre-de-rama

## 📥 Bajar cambios (Pull)

git pull

## 🔄 Actualizar rama con main

Parado dentro de tu rama de trabajo: 
git pull origin main

## 🧹 Limpiar archivos no deseados

git clean -f         # Eliminar archivos sin seguimiento
git clean -fd        # Eliminar archivos y carpetas sin seguimiento

## ✨ Comandos útiles para PBIP

Ver solo los cambios en archivos del modelo (JSON)
git diff -- Model/

Ver cambios del reporte:
git diff -- Report/




