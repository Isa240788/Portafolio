# 🌐 Dev Portafolio – Vue 3 + AOS

Landing page profesional desarrollada con Vue 3 `(Composition API + <script setup>`, animaciones con AOS, diseño moderno con Tailwind CSS y arquitectura modular basada en componentes.

Este proyecto presenta el perfil profesional, servicios y stack tecnológico de una desarrolladora Front-End.

## 🚀 Tecnologías Utilizadas

    ⚡ Vue 3

    🎨 Tailwind CSS

    🎬 AOS (Animate On Scroll)

    🎯 Heroicons

    ⭐ FontAwesome

    🧩 Componentización modular

    📱 Diseño Responsive (Mobile-first)

## 📁 Estructura del Proyecto

````text
src/
│
├── components/
│   ├── Navbar.vue
│   ├── Hero.vue
│   ├── About.vue
│   ├── Services.vue
│   └── Skills.vue
│
├── App.vue
└── main.js
````

Arquitectura basada en separación clara de responsabilidades y escalabilidad futura.

## 🧭 Navbar.vue

    Menú dinámico generado desde ref

    Navegación con scroll interno suave

    Menú hamburguesa animado en móvil

    Botón CTA “Hablemos”

    Diseño adaptable a todas las pantallas

    ✔ Estado reactivo con ref()
    ✔ Animaciones CSS puras
    ✔ Mobile-first

## 👋 Hero.vue

Sección principal del sitio:

    Presentación del nombre

    Rol profesional

    Descripción breve

    Botones CTA (Contacto + Descargar CV)

    Animaciones con fade-right y fade-up

    ✔ Microinteracciones en botones
    ✔ Gradiente moderno en texto
    ✔ Layout centrado verticalmente

## 🧑‍💻 About.vue

Sección descriptiva profesional:

    Trayectoria autodidacta

    Formación técnica

    Certificación Talento Digital (SENCE 2025–2026)

Botones dinámicos generados desde array

✔ Renderizado con v-for
✔ Animaciones escalonadas
✔ Diseño en grid responsive

## 🛠️ Services.vue

Sección de servicios con tarjetas dinámicas.

Características técnicas:

    Servicios definidos en array reactivo

    Renderizado dinámico

    Delay progresivo calculado con índice

    Tarjetas con microinteracciones avanzadas

    Grid adaptable (1 → 2 → 3 columnas)

    ✔ ref() para datos
    ✔ Animaciones AOS dinámicas
    ✔ Hover effects profesionales
    ✔ Preparado para conexión futura con API

## 💻 Skills.vue

Sección minimalista de habilidades técnicas.

Stack mostrado:

    Bootstrap

    Vue

    HTML5

    CSS3

    JavaScript

Características técnicas:

- Grid fluido:

    2 columnas móvil

    4 tablet

    6 desktop

    Renderizado dinámico desde array

    Iconos importados como objetos reales

    Microanimación scale en hover

Ejemplo estructura del array:

````text
const skills = [
  {
    id: 1,
    title: "Bootstrap",
    Icon: faBootstrap,
    iconColor: "text-purple-500"
  }
]
````

✔ Uso correcto de objetos de iconos
✔ Componentización limpia
✔ Diseño minimalista consistente

## 🎬 Animaciones

Configuradas globalmente en App.vue:

    duration: 800ms

    offset: 100

    easing: ease-in-out

    once: false

    Inicialización dentro de onMounted() usando nextTick() para asegurar render correcto del DOM.

## 📱 Responsividad

El proyecto sigue enfoque Mobile-first:

    Layouts con grid adaptable

    Botones en columna → fila

    Tipografía escalable

    Navbar transformable en menú fullscreen

## 🧠 Buenas Prácticas Aplicadas

✔ Composition API
✔ `<script setup>`
✔ Datos separados de la vista
✔ Renderizado dinámico
✔ Microinteracciones modernas
✔ Animaciones progresivas
✔ Código limpio y escalable
✔ Preparado para integración backend

## 🚀 Instalación

````text
# Clonar repositorio
git clone <url>

# Instalar dependencias
npm install

# Ejecutar en desarrollo
npm run dev
````

## 📈 Mejoras Futuras

Agregar sección de Proyectos dinámica

Implementar formulario funcional con EmailJS o backend propio

Optimización SEO

Lazy loading de componentes

Mejoras de accesibilidad (ARIA)

Modo oscuro/claro

Internacionalización (i18n)

## 📬 Contacto (Próximamente)

La sección Contacto será la encargada de permitir que reclutadores, clientes o colaboradores puedan comunicarse directamente desde el sitio web.

## 🎯 Objetivo

Facilitar el primer contacto profesional

Mejorar conversión del portafolio

Centralizar mensajes desde la web

## 🧩 Estructura Planeada

El componente futuro Contact.vue incluirá:

    Campo Nombre

    Campo Email

    Campo Mensaje

    Botón Enviar

    Validación básica de formulario

    Feedback visual (éxito / error)

## 🛠 Implementación Técnica Propuesta

- Opción 1 – EmailJS (sin backend)

    Integración rápida

    No requiere servidor propio

    Ideal para portafolios personales

## ✨ Mejoras Planeadas

    Validación con reglas reactivas

    Estados de carga (isSubmitting)

    Mensaje de confirmación animado

    Protección anti-spam (reCAPTCHA)

    Accesibilidad (ARIA labels)

    Sanitización de inputs

## 📁 Estructura futura

````text
components/
   Contact.vue
````

Y será agregado en App.vue debajo de Skills.

## 📌 Estado del Proyecto

    ✅ Navbar

    ✅ Hero

    ✅ About

    ✅ Services

    ✅ Skills

    🔄 Contact (En desarrollo)

## 👩‍💻 Autor

Desarrollado por Isabel – Front-End Developer
