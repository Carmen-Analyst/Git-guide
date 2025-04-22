
# 🚀 Cómo subir un proyecto a GitHub desde PyCharm usando SSH (Guía Rápida)

Esta guía documenta paso a paso cómo conecté PyCharm con GitHub mediante SSH, para subir proyectos sin usar usuario ni contraseña. ✅

---

## 🛠️ Requisitos previos

- Tener una cuenta en GitHub
- Tener Git y PyCharm instalados
- Tener configurado un proyecto local en PyCharm

---

## 🧭 PASOS SEGUIDOS

### 1. Crear una clave SSH

Desde la terminal del Mac:

```bash
ssh-keygen -t ed25519 -C "tu-correo-en-github@example.com"
```

Presiona `Enter` en las siguientes preguntas (usa la ruta por defecto y sin passphrase si prefieres).

### 2. Copiar la clave pública al portapapeles

```bash
pbcopy < ~/.ssh/id_ed25519.pub
```

### 3. Añadir la clave en GitHub

- Ir a [https://github.com/settings/keys](https://github.com/settings/keys)
- Clic en **New SSH Key**
- Pegar la clave copiada
- Guardar

---

## 🔁 Conectar PyCharm a GitHub

### 4. Crear un nuevo repositorio en GitHub (SIN README, ni .gitignore, ni licencia)

### 5. Inicializar Git en el proyecto local desde PyCharm

```bash
git init
git add .
git commit -m "Primer commit"
```

### 6. Cambiar la URL remota a SSH

```bash
git remote add origin git@github.com:TU_USUARIO/TU_REPO.git
```

(Sustituye por tu usuario y nombre de repo)

---

## ☁️ Subir el proyecto a GitHub

```bash
git push -u origin main
```

Si es la primera vez, escribe:

```bash
yes
```

cuando te pregunte si confías en GitHub.

---

## 🎉 Resultado

El proyecto ya está publicado en GitHub, y no volverá a pedirte usuario ni contraseña gracias a la autenticación SSH 🔐

---

_Creado por Carmen-analyst — publicado desde PyCharm con ❤️_
