# CONTINUIDAD – PROYECTO RYKUO WEB

## 1️⃣ Objetivo
Guía rápida para que un nuevo desarrollador pueda **entender, mantener y continuar** Rykuo Web sin depender del dev original.

---

## 2️⃣ Estructura del Repositorio


rykuo-web/
├── public/ # Imágenes, videos, favicon
├── src/
│ ├── components/ # Componentes reutilizables
│ │ ├── layout/ # Header, Footer
│ │ └── sections/ # Hero, About, Products, Services, CTA, BackHome
│ ├── layouts/ # BaseLayout.astro
│ ├── pages/ # Páginas (.astro)
│ └── styles/ # global.css / Tailwind
├── .env.example # Variables de entorno
├── package.json # Dependencias y scripts
├── astro.config.mjs
└── tsconfig.json


---

## 3️⃣ Cómo Agregar Funcionalidades

- **Nueva página:** Crear `.astro` en `src/pages/`, envolver con `<BaseLayout>`  
- **Nuevo componente:** Crear `.astro` en `components/sections/`, importar en la página correspondiente  
- **Variables de entorno:** Actualizar `.env` a partir de `.env.example`  

---

## 4️⃣ Flujo General

1. Cada página importa los componentes que necesita.  
2. Cotizador dinámico calcula totales según productos seleccionados.  
3. Formulario de contacto envía mensajes correctamente vía Resend.  
4. Google Analytics mide visitas desde layout global.  

---

## 5️⃣ Bugs Conocidos

- **Responsive en móviles muy pequeños:** Algunas secciones (Hero, CTA) requieren ajustes de CSS.  
- **Cotizador:** Funciona correctamente solo si se seleccionan productos (comportamiento esperado).  
- **Formulario:** Envía mensajes correctamente, sin errores conocidos.  

---

## 6️⃣ Recomendaciones

- Mantener arquitectura modular de Astro.  
- Seguir consistencia en nombres de archivos (`CamelCase` para componentes).  
- Documentar cambios en `CONTINUIDAD.md` y commits.  
- Ejecutar `npm run build` antes de subir a producción.  