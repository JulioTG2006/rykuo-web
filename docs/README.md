# 🌐 Rykuo – Sitio Web Corporativo

Proyecto web corporativo desarrollado con Astro y Tailwind CSS, orientado a la presentación de productos industriales y a la implementación de un sistema de cotización interactivo sin backend.

---

## 📌 Descripción del Proyecto

El sitio web de **Rykuo** fue desarrollado como una solución moderna, rápida y escalable para la presentación de productos industriales.

El proyecto incluye:

- Catálogo de productos organizado por categorías
- Sistema de filtrado dinámico
- Cotizador interactivo en tiempo real
- Formulario de contacto funcional sin backend
- Diseño responsive adaptable a dispositivos móviles
- Google Analytics control de usuarios

---

## 🎯 Objetivos

### Objetivo General
Desarrollar un sitio web corporativo moderno con funcionalidades dinámicas utilizando tecnologías frontend actuales.

### Objetivos Específicos

- Implementar catálogo de productos filtrable.
- Desarrollar un sistema de cotización automática.
- Permitir cálculo dinámico según cantidad.
- Implementar formulario de contacto funcional.
- Aplicar buenas prácticas de estructura y organización.

---

## 🛠 Tecnologías Utilizadas

- **Astro** – Framework principal para generación estática.
- **Tailwind CSS** – Framework de estilos.
- **JavaScript (Vanilla)** – Lógica interactiva del cotizador.
- **Formspree** – Servicio externo para envío de correos.
- **HTML5 / CSS3**
- **Google Analytics**– Control de Usuarios tiempo real 

---

## 🏗 Arquitectura del Proyecto

El proyecto utiliza **Static Site Generation (SSG)** con Astro.

No se implementó backend propio.  
Las funcionalidades dinámicas se manejan del lado del cliente.

### 📂 Estructura del Proyecto


```
```



---
```
rykuo-web/
├── src/
│   ├── layouts/
│   │   ├
│   │   └── BaseLayout.astro
│   ├── components/
│   │   ├── Header.astro
│   │   ├── Footer.astro
│   │   ├── NavBar.astro
│   │   ├── ProductCard.astro
│   │   ├── ProductFilter.astro
│   │   ├── QuotationForm.astro
│   │   └── ContactForm.astro
│   ├── pages/
│   │   ├── index.astro
│   │   ├── productos.astro
│   │   ├── servicios.astro
│   │   ├── cotizacion.astro
│   │   ├── sobre-nosotros.astro
│   │   └── contacto.astro
│   ├── styles/
│   │   └── globals.css
│   └── scripts/
│       ├── quotation.js
│       └── filter.js
├── public/
│   ├── images/
│   │   ├── products/
│   │   └── logos/
│   └── favicon.svg
├── astro.config.mjs
├── tailwind.config.js
├── package.json
└── README.md
```

## ⚙ Funcionalidades Implementadas

### 1️⃣ Catálogo de Productos

- 15 productos organizados en:
  - Motores
  - Automatización
  - Control
- Sistema de filtrado por categoría.
- Diseño visual moderno y responsivo.

---

### 2️⃣ Cotización Inteligente

- Selección dinámica de producto.
- Obtención automática del precio mediante atributos `data-*`.
- Cálculo en tiempo real según cantidad ingresada.
- Actualización inmediata del total estimado.
- Interfaz simple e intuitiva.

---

### 3️⃣ Formulario de Contacto

- Envío de mensajes sin backend.
- Integración con servicio externo (Formspree).
- Confirmación de envío.
- Compatible con despliegue estático.

---

## 💡 Innovación del Proyecto

Se implementó un sistema de cotización interactiva sin necesidad de servidor backend, utilizando únicamente JavaScript del lado del cliente.

Esto permite:

- Reducir costos de infraestructura.
- Mantener alta velocidad de carga.
- Simplificar el despliegue en hosting estático.
- Mejorar experiencia del usuario.

---

## 🚀 Instalación y Ejecución

1. Clonar el repositorio:


git clone <URL_DEL_REPOSITORIO>


2. Instalar dependencias:


npm install


3. Ejecutar en modo desarrollo:


npm run dev


4. Generar versión para producción:


npm run build


---

## 📱 Responsive Design

El sitio fue desarrollado utilizando Tailwind CSS, asegurando:

- Adaptabilidad a dispositivos móviles.
- Diseño limpio y minimalista.
- Experiencia de usuario optimizada.

---

## 📈 Buenas Prácticas Aplicadas

- Separación de layouts y componentes.
- Organización modular del código.
- Uso de atributos `data-*` para lógica dinámica.
- Estructura limpia y escalable.
- Código mantenible y documentado.

---

## 🧠 Conclusión

El proyecto cumple con los objetivos planteados, implementando una solución web moderna, eficiente y funcional.

Se logró integrar interactividad avanzada sin backend, demostrando dominio de tecnologías frontend y buenas prácticas de desarrollo web.

---

## 👨‍💻 Autor

Desarrollado por: **Julio Samuel Torres Garate**  
Especialidad: Desarrollo de Software  
Año: 2026