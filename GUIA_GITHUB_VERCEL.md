# 🚀 Guía: GitHub → Vercel para Dashboard Mundial 2026

## Paso 1: Preparar los archivos localmente

```bash
# 1. Crear carpeta del proyecto
mkdir mundial-2026-dashboard
cd mundial-2026-dashboard

# 2. Copiar los archivos aquí:
# - dashboard_mundial_2026_mejorado.html (renombrarlo a index.html)
# - README.md
# - .gitignore
```

**Importante**: Renombra el archivo HTML a `index.html` (Vercel lo busca automáticamente)

```bash
# Si está descargado, muévelo así:
mv dashboard_mundial_2026_mejorado.html index.html
```

---

## Paso 2: Inicializar Git localmente

```bash
# Desde la carpeta del proyecto
git init
git add .
git commit -m "Inicial: Dashboard Mundial 2026"
```

---

## Paso 3: Crear repositorio en GitHub

### Opción A: Desde GitHub (Recomendado)

1. Ve a [github.com/new](https://github.com/new)
2. Completa:
   - **Repository name**: `mundial-2026-dashboard`
   - **Description**: `Dashboard interactivo Nike vs Adidas - Mundial 2026`
   - **Public** (✓ selecciona público)
   - **Add .gitignore**: No necesario (ya lo tienes)
   - **Add README**: No (ya lo tienes)

3. Click en **"Create repository"**

---

## Paso 4: Conectar repo local con GitHub

GitHub te mostrará instrucciones. Copia y ejecuta en tu terminal:

```bash
# Agregar el origen remoto
git branch -M main
git remote add origin https://github.com/TU_USUARIO/mundial-2026-dashboard.git

# Hacer push
git push -u origin main
```

**Reemplaza `TU_USUARIO`** con tu usuario de GitHub

---

## Paso 5: Conectar con Vercel

### Opción A: Desde Vercel (Automático - Recomendado)

1. Ve a [vercel.com/new](https://vercel.com/new)
2. Selecciona **"Import Git Repository"**
3. Pega tu URL de GitHub:
   ```
   https://github.com/TU_USUARIO/mundial-2026-dashboard
   ```
4. Click **"Continue"**
5. Vercel auto-detectará tu proyecto (no necesita config especial para HTML puro)
6. Click **"Deploy"** ✅

### Opción B: Desde GitHub (Alternativa)

1. En tu repo de GitHub: Settings → GitHub Apps → Vercel
2. Autoriza la conexión
3. Vercel tomará la configuración automáticamente

---

## Paso 6: ¡Listo! 🎉

Vercel te generará un link como este:

```
https://mundial-2026-dashboard.vercel.app
```

O un link temporal:
```
https://mundial-2026-dashboard-[random].vercel.app
```

---

## 🔄 Actualizar el Dashboard

Cada vez que hagas cambios:

```bash
# Editar index.html (o los archivos que necesites)

# Subir cambios a GitHub
git add .
git commit -m "Descripción del cambio"
git push

# Vercel detectará el push automáticamente y redesplegará
# (En ~1 minuto estará actualizado en el link público)
```

---

## ✅ Checklist Final

- [ ] Carpeta local con `index.html`, `README.md`, `.gitignore`
- [ ] Git inicializado localmente (`git init`)
- [ ] Repositorio creado en GitHub
- [ ] Push hecho a GitHub (`git push`)
- [ ] Vercel conectado y desplegado
- [ ] Link público accesible desde navegador

---

## 🆘 Troubleshooting

### "Error: File not found" en Vercel
→ Asegúrate que el archivo se llama `index.html` (no HTML mayúsculas, no con números)

### "404 Not Found"
→ El deploy puede tardar 1-2 minutos. Espera y recarga.

### Vercel no detecta cambios
→ Vercel solo redeploya cuando hace push a GitHub. Asegúrate de hacer `git push`

### "Permission denied (publickey)"
→ Configura SSH en GitHub o usa HTTPS en lugar de SSH

```bash
# Ver configuración actual
git remote -v

# Cambiar a HTTPS (si está en SSH)
git remote set-url origin https://github.com/TU_USUARIO/mundial-2026-dashboard.git
```

---

## 📱 Prueba el Link

Una vez desplegado en Vercel:
- ✅ Abre desde computadora
- ✅ Abre desde móvil
- ✅ Comparte el link con otros
- ✅ Inserta en un iFrame si lo necesitas

---

## 🎯 Próximos pasos opcionales

1. **Dominio personalizado**: Settings → Domains en Vercel
2. **Agregar formulario**: Conectar Vercel con un servicio como Formspree
3. **Analytics**: Habilitar Vercel Analytics para ver tráfico
4. **Environment Variables**: Si agregás backend más adelante

---

¿Listo? ¡Comienza por el Paso 1! 🚀
