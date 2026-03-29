# 🛒 Lista del Super — App Android

App de lista de compras con presupuesto, promociones y guardado automático.

---

## 📲 Cómo generar el APK con GitHub (GRATIS, sin instalar nada)

### Paso 1 — Crear cuenta en GitHub
1. Entrá a **github.com** y creá una cuenta gratuita (si no tenés)

### Paso 2 — Crear un repositorio nuevo
1. En GitHub, hacé clic en el botón verde **"New"** (o el **"+"** arriba a la derecha)
2. Poné de nombre: `lista-del-super`
3. Dejalo en **Public** (necesario para la compilación gratuita)
4. NO marques ninguna opción extra (sin README, sin .gitignore)
5. Hacé clic en **"Create repository"**

### Paso 3 — Subir los archivos
1. En la página del repositorio vacío, hacé clic en **"uploading an existing file"**
2. Arrastrá TODOS los archivos y carpetas de este ZIP al área de carga
   - ⚠️ Importante: subí también las carpetas `.github/` y todo su contenido
3. En la parte de abajo escribí un mensaje como "Primera versión"
4. Hacé clic en **"Commit changes"**

### Paso 4 — Esperar la compilación automática
1. Una vez subidos los archivos, GitHub va a compilar la app automáticamente
2. Hacé clic en la pestaña **"Actions"** del repositorio
3. Vas a ver un proceso corriendo llamado **"Build APK"** con un círculo amarillo ⏳
4. Esperá unos **3-5 minutos** hasta que se ponga verde ✅

### Paso 5 — Descargar el APK
1. Hacé clic en el proceso verde **"Build APK"**
2. Abajo de todo vas a ver una sección **"Artifacts"**
3. Hacé clic en **"lista-del-super-apk"** para descargar el APK
4. Se descarga un ZIP que adentro tiene el archivo `app-debug.apk`

### Paso 6 — Instalar en Android
1. Pasá el archivo `app-debug.apk` a tu celular (por WhatsApp, Drive, cable, etc.)
2. En el celu, antes de instalarlo activá los "Orígenes desconocidos":
   - Configuración → Seguridad → Instalar apps desconocidas → Chrome (o el app desde donde lo abrís)
3. Tocá el archivo APK y seguí los pasos de instalación
4. ¡Listo! La app aparece en tu menú como **"Lista del Super"** 🛒

---

## ❓ Preguntas frecuentes

**¿Es gratis?**
Sí, 100% gratis. GitHub da minutos de compilación gratuitos más que suficientes.

**¿Cuánto pesa el APK?**
Aproximadamente 2-4 MB.

**¿Funciona sin internet?**
Sí, la app funciona completamente offline. No necesita internet para nada.

**¿Los datos se guardan?**
Sí, todo se guarda automáticamente en el dispositivo usando localStorage.

**¿Puedo actualizar la app?**
Sí. Si en el futuro querés actualizar la app, reemplazás el archivo `app/src/main/assets/index.html` en GitHub con la nueva versión del HTML y automáticamente se vuelve a compilar un APK nuevo.

---

## 📁 Estructura del proyecto

```
superapp/
├── .github/
│   └── workflows/
│       └── build.yml          ← Instrucciones para GitHub Actions
├── app/
│   ├── src/
│   │   └── main/
│   │       ├── assets/
│   │       │   └── index.html ← La app completa
│   │       ├── java/com/listasuper/app/
│   │       │   └── MainActivity.java
│   │       ├── res/
│   │       │   ├── layout/activity_main.xml
│   │       │   ├── mipmap-*/ic_launcher.png (íconos)
│   │       │   └── values/strings.xml
│   │       └── AndroidManifest.xml
│   └── build.gradle
├── gradle/wrapper/
│   └── gradle-wrapper.properties
├── gradlew
├── gradlew.bat
├── build.gradle
├── settings.gradle
└── gradle.properties
```

---

Hecho con ❤️ — Lista del Super v1.0
