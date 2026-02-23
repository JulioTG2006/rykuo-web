# ESTRUCTURA DE DOCUMENTACIÓN – PROYECTO RYKUO WEB

## 1️⃣ Información General del Proyecto

**Nombre del Proyecto:** Rykuo Web  
**Desarrollador / Equipo:** Julio Samuel Torres Garate  
**Carrera:** Desarrollo y diseño de Software  
**Versión:** v1.0  
**Fecha de entrega:** 23/02/2026  
**Repositorio Oficial:** https://github.com/diegomejiam/Rykuo-Web 


## Arquitectura del Sistema

- Arquitectura modular basada en componentes  
- Generación estática (SSG)  
- Layout global (BaseLayout.astro)  
- Componentes reutilizables (Hero, About, Products, Services, CTA, etc.)  
- Separación clara de capas: `components/`, `pages/`, `styles/`, `public/`  

**Flujo del Sistema:**  
Usuario → Página (Astro) → Layout global → Componentes → JS dinámico → Google Analytics → HTML optimizado

---

## Tecnologías Utilizadas

- **Astro:** Framework principal, renderizado SSG  
- **Tailwind CSS:** Estilos y diseño responsivo  
- **JavaScript:** Interactividad y cotización dinámica  
- **Google Analytics:** Seguimiento de visitas y comportamiento  
- **HTML5 / CSS3:** Estructura y estilos base  

---

## Estructura de Carpetas


rykuo-web/
├── public/
│ ├── images/
│ ├── video/
│ ├── favicon.ico
│ └── robots.txt
├── src/
│ ├── components/
│ │ ├── layout/
│ │ │ ├── Header.astro
│ │ │ └── Footer.astro
│ │ └── sections/
│ │ ├── Hero.astro
│ │ ├── About.astro
│ │ ├── Products.astro
│ │ ├── Services.astro
│ │ ├── CTA.astro
│ │ └── BackHome.astro
│ ├── layouts/
│ │ └── BaseLayout.astro
│ ├── pages/
│ │ ├── index.astro
│ │ ├── sobre-nosotros.astro
│ │ ├── productos.astro
│ │ ├── servicios.astro
│ │ ├── cotizacion.astro
│ │ └── contacto.astro
│ └── styles/
│ └── global.css
├── .env.example
├── astro.config.mjs
├── tsconfig.json
└── package.json


---

## Flujo de Trabajo

1. Usuario accede a la ruta → Astro procesa página  
2. BaseLayout se aplica  
3. Componentes se renderizan  
4. JS ejecuta funcionalidad dinámica (cotización, formulario)  
5. Google Analytics registra visitas y comportamiento  
6. HTML final optimizado se entrega al navegador  
