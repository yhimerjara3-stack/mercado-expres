# Mercado Exprés - Tienda Móvil & Proyecto APK Android

Aplicación completa de comercio y abarrotes con soporte PWA, geolocalización GPS, panel administrativo, pedidos por WhatsApp y empaquetador para Android APK.

---

## 🚀 1. Instalación y Ejecución en Desarrollo

1. Abre una terminal en esta carpeta y ejecuta:
   ```bash
   npm install
   ```

2. Inicia el servidor local:
   ```bash
   npm run dev
   ```
   Abre [http://localhost:3000](http://localhost:3000) en tu navegador.

3. Para compilar la versión web:
   ```bash
   npm run build
   ```

---

## 📱 2. Compilar Archivo APK con Android Studio (Capacitor)

1. En la misma carpeta ejecuta:
   ```bash
   # Instalar dependencias de Android
   npm install @capacitor/core @capacitor/cli @capacitor/android

   # Compilar el proyecto web a la carpeta dist/
   npm run build

   # Añadir la plataforma nativa de Android
   npx cap add android

   # Abrir el proyecto en Android Studio
   npx cap open android
   ```

2. En Android Studio:
   - Espera que termine de sincronizar Gradle.
   - Ve al menú superior: **Build** > **Build Bundle(s) / APK(s)** > **Build APK(s)**.
   - ¡Listo! En la notificación inferior haz clic en **"locate"** para ver tu archivo `app-debug.apk`.

---

## 🌐 3. Publicar este proyecto en GitHub y la Web

### Paso 1: Subir a GitHub
Abre la terminal en la carpeta del proyecto y corre:
```bash
git init
git add .
git commit -m "Initial commit - Mercado Expres UNASAM"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/mercado-expres.git
git push -u origin main
```

### Paso 2: Publicar tu página gratis (Vercel o GitHub Pages)
- **Opción recomendada (Vercel con 1 clic):**
  1. Entra a [https://vercel.com](https://vercel.com) e inicia sesión con tu cuenta de GitHub.
  2. Haz clic en **Add New Project** y selecciona tu repositorio `mercado-expres`.
  3. Haz clic en **Deploy**. ¡Tu página estará pública en 30 segundos con enlace HTTPS propio!

- **Opción GitHub Pages:**
  1. En tu repositorio de GitHub, ve a **Settings** > **Pages**.
  2. En Source selecciona **GitHub Actions** > **Static HTML** o usa el comando `npx gh-pages -d dist`.

---

## ⚙️ 4. Credenciales de Administrador
- **PIN por defecto:** `1234`
- **Número de atención por WhatsApp:** Configurable en `src/components/OrderConfirmationModal.tsx`
