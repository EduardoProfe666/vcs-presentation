---
title: VCS
titleTemplate: '%s - Conferencia JCE'
description: Conferencia de control de versiones distribuido para la JCE Informática 2025
keywords: vcs, git, github, jce, informatica, eltoque
info: Conferencia de control de versiones distribuido para la JCE Informática 2025
author: AICA+
favicon: /favicon.ico

theme: seriph

highlighter: shiki
lineNumbers: false

class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true

addons:
  - fancy-arrow
  - slidev-component-spotlight
  - slidev-component-scroll
---

<div class="background-container"></div>

# <span class="fade-in">Control de Versiones Distribuido</span>


### <span class="fade-in">VCS, Git, GitHub, Devops</span>

<div class="text-xl text-gray-200 mt-4 fade-in">
Caso de estudio: Aplicación web para el análisis de las tasas de cambio de divisas en el mercado informal cubano,
con tecnología de elToque
</div>

<div class="abs-br m-6 text-xl fade-in flex space-x-4">
  <a href="https://github.com/EduardoProfe666/vcs-presentation" target="_blank" class="slidev-icon-btn" aria-label="Código fuente presentación GitHub">
    <carbon:logo-github />
  </a>
  <a href="https://tasas-cuba.vercel.app/" target="_blank" class="slidev-icon-btn" aria-label="Ir a la aplicación tasas-cuba">
    <carbon:app />
  </a>

  <a href="https://github.com/EduardoProfe666/tasas-cuba" target="_blank" class="slidev-icon-btn" aria-label="Código fuente de la aplicación tasas-cuba en GitHub">
    <carbon:kubernetes-pod />
  </a>
</div>

<footer style="color: #05d8f3; font-weight: bold;" class="fade-in abs-b m-6">
  <a href="https://eduardoprofe666.github.io" target="_blank">Ing. Eduardo Alejandro Gonzalez Martell</a>
</footer>

<style>
  .background-container {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url('/banner-inicio.webp');
    background-size: cover;
    background-position: center;
    filter: blur(8px);
    z-index: -1;
  }

  .fade-in {
      animation: fadeIn 1s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  span {
    background-color: #81dbff;
    background-image: linear-gradient(45deg, #89effd 20%, #46c0ed 50%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
  }
</style>

---
layout: center
transition: slide-left
---

<div class="image"></div>

<style>
  .image {
    content: "";
    position: fixed;
    top: 20px;
    left: 20px;
    right: 20px;
    bottom: 20px;
    background-image: url('/folders.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    z-index: -1;
    pointer-events: none;
  }
</style>


---
layout: center
class: text-center p-12
transition: slide-up
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">¿Qué es un VCS?</span>

<section>
  <v-click>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h3 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Un sistema de control de versiones (VCS) registra los cambios en archivos a lo largo del tiempo, permitiéndote recuperar versiones anteriores cuando las necesites.
          </h3>
        </div>
    </div>
  </v-click>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-up
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">¿Qué permite hacer un VCS?</span>

<section>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
            <div class="space-y-8 text-xl font-semibold leading-relaxed drop-shadow-md list-none">
                  <v-click><p>✅ Permite volver a versiones anteriores de archivos o del proyecto, disminuyendo significativamente el nivel de estrés post-traumático.</p></v-click>
                  <v-click><p>🕵️‍♂️ Facilita comparar los cambios en el tiempo, pudiendo saber quién tiene la culpa de que el proyecto no funcione.</p></v-click>
                  <v-click><p>💾 Si tu computadora se rompe, se corrompe el proyecto o se va la luz, permite recuperar todo sin llorar mucho.</p></v-click>
                  <v-click><p>🤝 Si estás trabajando con otros, gestiona los cambios simultáneos sin conflictos, tanto de código como personales.</p></v-click>
            </div>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-left
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Clasificación</span>

<section>
    <div>
    <v-click>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h2 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Locales
          </h2>
        </div>
    </div>
    </v-click>
    </div>
    <div></div>
    <div>
    <v-click>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h2 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Centralizados
          </h2>
        </div>
    </div>
    </v-click>
    </div>
    <div></div>
    <div>
    <v-click>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h2 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Distribuidos
          </h2>
        </div>
    </div>
    </v-click>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: two-cols
class: text-center p-12
transition: slide-up
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">VCS Locales</span>

<section>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h3 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Manejan una simple base de datos en local que lleva el registro de todos los cambios 
            realizados en los archivos. Un ejemplo de VCS local es RCS.
          </h3>
        </div>
    </div>
</section>

::right::

<div class="flex fade-in items-center justify-center h-full">
  <img class="h-90" src="/local.png" alt="local" />
</div>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-left
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Desventajas</span>

<section>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
            <div class="space-y-8 text-xl font-semibold leading-relaxed drop-shadow-md list-none">
                  <v-click><p>📁 Si se va a la luz, se corrompe la bd o la computadora muere, ¡adiós proyecto!</p></v-click>
                  <v-click><p>🚫 Nadie puede colaborar contigo, si tienes un problema eres tú contra ese proyecto en soledad.</p></v-click>
                  <v-click><p>🐢 Si el proyecto crece, el desarrollo se vuelve lento, todo depende de tu PC de la NASA.</p></v-click>
            </div>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: two-cols
class: text-center p-12
transition: slide-up
---

<div class="flex fade-in items-center justify-center h-full">
  <img class="h-90" src="/central.png" alt="central" />
</div>

::right::

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">VCS Centralizados</span>

<section>
    <div class="m-2 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-5 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h3 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Todo se almacena en un único repositorio central en un servidor,
            desde donde los desarrolladores descargan copias locales para trabajar y luego suben sus cambios para
            crear nuevas versiones.
          </h3>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-left
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Desventajas</span>

<section>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
            <div class="space-y-8 text-xl font-semibold leading-relaxed drop-shadow-md list-none">
                  <v-click><p>🖥️ Si el servidor muere, ¡adiós proyecto!</p></v-click>
                  <v-click><p>🔒 Solo uno puede tocar un archivo a la vez, por lo que si alguien lo bloquea te toca esperar.</p></v-click>
                  <v-click><p>🐢 Todo pasa por un solo lugar, por lo que todo depende de cuánto dinero le hayas puesto al servidor.</p></v-click>
                  <v-click><p>🤹‍♂️ Cuando logras subir tus cambios, puede que haya un sinfín de conflictos que hay que arreglar rápido para que el equipo no se atrase.</p></v-click>
                  <v-click><p>⚡ Si a todo esto le sumamos Etecsa y su magnífica conexión...</p></v-click>
            </div>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: two-cols
class: text-center p-12
transition: slide-up
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">VCS Distribuidos</span>

<section>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h3 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Todos los desarrolladores tienen su propia copia del repositorio, con todas las versiones y 
            toda la historia
          </h3>
        </div>
    </div>
</section>

::right::

<div class="flex fade-in items-center justify-center h-full">
  <img class="h-90" src="/distribuido.png" alt="distribuido" />
</div>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-left
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Solo Ventajas</span>

<section>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
            <div class="space-y-8 text-xl font-semibold leading-relaxed drop-shadow-md list-none">
                  <v-click><p>🖥️ Puedes hacer cambios y operaciones desde tu laptop sin conectarte.</p></v-click>
                  <v-click><p>⚡ Todas las operaciones son instantáneas, no tienes que esperar que el servidor responda .</p></v-click>
                  <v-click><p>🛡️ Si el servidor central se cae, o se te rompe la laptop, cada quien tiene el respaldo del repositorio completo.</p></v-click>
            </div>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: two-cols
class: text-center p-12
transition: slide-up
---

<div class="flex fade-in items-center justify-center h-full">
  <img class="h-90" src="/vcs.png" alt="central" />
</div>

::right::

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Git</span>

<section>
    <div class="m-2 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-5 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h4 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Creado en abril de 2005 por Linus Torvalds para gestionar eficientemente el código del kernel de Linux,
            tras perder acceso a BitKeeper. Hoy es el VCS más popular del mundo, siendo usado por más de 100 millones
            de desarrolladores en proyectos tanto comerciales como de código abierto
          </h4>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
transition: slide-up
class: text-center
layout: center
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Instalando Git</span>

<section>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
            <div class="space-y-8 text-xl font-semibold leading-relaxed drop-shadow-md list-none">
                  <v-click><p>🍎 <em>MacOS:</em> <code>brew install git</code>.</p></v-click>
                  <v-click><p>🐧 <em>Fedora Distros:</em> <code>yum install git-core</code>.</p></v-click>
                  <v-click><p>🌀 <em>Debian Distros:</em> <code>apt-get install git-core</code>.</p></v-click>
                  <v-click><p>🪟 <em>Windows:</em> Descargar el instalador y seguir las instrucciones en <a href="https://git-scm.com/download/win">git-scm/windows</a>.</p></v-click>
            </div>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
transition: slide-left
class: text-center
layout: center
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Configurando Git</span>

<section>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
            <div class="space-y-8 text-xl font-semibold leading-relaxed drop-shadow-md list-none">
                  <v-click><p>👤 <em>Nombre:</em> <code>git config --global user.name "Eduardo González"</code>.</p></v-click>
                  <v-click><p>📧 <em>Email:</em> <code>git config --global user.email "eduardoprofe666@gmail.com"</code>.</p></v-click>
                  <v-click><p>⚙️ <em>Revisa la configuración:</em> <code>git config --list</code>. Esta se guarda en el Home en <code>.gitconfig</code></p></v-click>
                  <v-click><p>❓ <em>Ayuda:</em> <code>git config --help</code>o en  <a href="https://git-scm.com/docs">git-scm/docs</a>.</p></v-click>
            </div>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center
transition: slide-up
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Principales Conceptos y Comandos</span>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: two-cols
class: text-center p-12
transition: slide-up
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Repositorios</span>

<section>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h4 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Un repositorio es una carpeta o conjunto de carpetas que contienen archivos. Es la unidad fundamental
            de <em>Git</em>. <br> Para crear un repositorio usa <code>git init .</code>
          </h4>
        </div>
    </div>
</section>

::right::

<div class="flex fade-in items-center justify-center h-full">
  <img class="h-90" src="/repositorio.png" alt="repo" />
</div>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: two-cols
class: text-center p-12
transition: slide-up
---

<div class="flex fade-in items-center justify-center h-full">
  <img class="h-90" src="/status.png" alt="status" />
</div>

::right::

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Estado del Repositorio</span>

<section>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h4 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Usando <code>git status</code> se puede saber que cambios hay actualmente en el repositorio
            con respecto a la versión anterior.
          </h4>
        </div>
    </div>
</section>


<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-up
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Add y Commit</span>

<section class="flex gap-8 justify-center">
    <div class="m-8 w-1/2 bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h2 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Add
          </h2>
          <h4 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            El comando <code>git add .</code> permite confirmar que todos los cambios realizados se quieren salvar.
          </h4>
        </div>
    </div>
    <div class="m-8 w-1/2 bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h2 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Commit
          </h2>
          <h4 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            El comando <code>git commit -m "Commit Inicial"</code> permite consolidar los cambios confirmados como una version nueva, especificando un mensaje informativo.
          </h4>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-up
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">¿Cómo nombrar commits?</span>

<section class="flex gap-2 justify-center">
    <v-click>
    <div class="m-2  w-1/2 bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h2 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Versionado Semántico
          </h2>
          <h4 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Estándar que utiliza un formato de tres números para comunicar de forma clara y consistente el tipo de cambios realizados en una versión de software, facilitando así la gestión y compatibilidad entre proyectos.  
            <br>
            Por ejemplo <code>1.0.0 < 2.0.0 < 2.1.0 < 2.1.1.</code>
            <br>
            Encuentra más información en <a href="https://semver.org/lang/es/">semver.org</a>.
          </h4>
        </div>
    </div>
    </v-click>
    <v-click>
    <div class="m-2  w-1/2 bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h2 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Commits Convencionales
          </h2>
          <h4 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Convención para escribir mensajes de commit con un formato claro y estructurado que facilita la comprensión tanto para personas como para máquinas. 
            <br>
            Se usan etiquetas como <code>feat</code>, <code>fix</code>, <code>refactor</code> y <code>chore</code>.
            <br>
            Encuentra más información en <a href="https://www.conventionalcommits.org/es/v1.0.0/">conventionalcommits.org</a>.
          </h4>
        </div>
    </div>
    </v-click>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-up
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Ramas</span>

<section class="flex gap-2 justify-center">
    <div class="m-8 w-1/2 bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h2 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            ¿Qué es una rama?
          </h2>
          <h4 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Una rama en Git es un puntero a un commit. La rama por defecto es <code>master</code> o <code>main</code>. Con el primer commit que realicemos, se creará esta rama principal apuntando a ese commit. En cada commit que realicemos, la rama irá avanzando automáticamente. 
          </h4>
        </div>
    </div>
    <div class="m-8 w-1/2 bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h2 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Comandos útiles
          </h2>
            <div class="space-y-8 text-lg font-semibold leading-relaxed drop-shadow-md list-none">
                  <p>🌱 <em>Crear rama:</em> <code>git branch development</code>.</p>
                  <p>📋 <em>Listar ramas:</em> <code>git branch</code>.</p>
                  <p>🔀 <em>Cambiar entre ramas:</em> <code>git checkout hotfix</code>.</p>
                  <p>🪢 <em>Fusionar cambios:</em> <code>git merge master</code>.</p>
            </div>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-up
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Estrategias para <em>branching</em></span>

<section class="flex gap-2 justify-center">
    <v-click>
    <div class="m-2  w-1/2 bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h2 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Git Flow
          </h2>
          <h4 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Propuesta por Vincent Driessen, es una estrategia estructurada que usa varias ramas:
            <div class="space-y-4 text-md font-semibold leading-relaxed drop-shadow-md list-none">
                  <p>🌿 <em>Producción:</em> <code>main</code> o <code>master</code>.</p>
                  <p>🔄 <em>Integración de funcionalidades:</em> <code>develop</code> o <code>dev</code>.</p>
                  <p>✨ <em>Nuevas funcionalidades:</em> <code>feature</code>.</p>
                  <p>🏷️ <em>Preparar versiones:</em> <code>release</code>.</p>
                  <p>🚑 <em>Correcciones urgentes en producción:</em> <code>hotfix</code>.</p>
            </div>
          </h4>
        </div>
    </div>
    </v-click>
    <v-click>
    <div class="m-2  w-1/2 bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h2 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Trunk-Based Development
          </h2>
          <h4 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Todos los desarrolladores trabajan en una sola rama principal (<code>trunk</code> o <code>main</code>), integrando
            cambios frecuentemente con ramas de corta duración para nuevas funcionalidades o correcciones.
          </h4>
        </div>
    </div>
    </v-click>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-up
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Trabajo en Remoto</span>

<section class="flex gap-2 justify-center">
    <div class="m-4 w-1/2 bg-white bg-opacity-20 rounded-xl p-4 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h2 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            ¿Qué es una remote?
          </h2>
          <h4 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Es un alias que apunta a un repositorio externo, generalmente alojado en un servidor como GitHub, con el cual tu repositorio local se conecta para enviar y recibir cambios. Funciona como un marcador que facilita la colaboración y sincronización entre desarrolladores sin acceso en tiempo real directo al repositorio remoto. 
            <br>
            Por lo general se conoce como <code>origin</code>.
          </h4>
        </div>
    </div>
    <div class="m-4 w-1/2 bg-white bg-opacity-20 rounded-xl p-4 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h2 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Comandos útiles
          </h2>
            <div class="space-y-8 text-lg font-semibold leading-relaxed drop-shadow-md list-none">
                  <p>🛠️ <em>Clonar repo remoto:</em> <code>git clone <em>repo</em></code>.</p>
                  <p>📤 <em>Subir cambios pendientes:</em> <code>git push</code>.</p>
                  <p>👀 <em>Obtener cambios de remoto:</em> <code>git fetch origin</code>.</p>
                  <p>📥 <em>Fusionar cambios de remoto:</em> <code>git pull</code>.</p>
            </div>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
transition: slide-up
class: text-center
layout: center
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Otros Comandos</span>

<section>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
            <div class="space-y-8 text-xl font-semibold leading-relaxed drop-shadow-md list-none">
                  <v-click><p>👀 <em>Diferencias entre versiones:</em> <code>git diff</code>.</p></v-click>
                  <v-click><p>📜 <em>Historial de cambios:</em> <code>git log</code>.</p></v-click>
                  <v-click><p>🔄 <em>Cancelar los cambios:</em> <code>git checkout -- file</code>.</p></v-click>
            </div>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-left
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Recurso para aprender Git</span>

<section>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h3 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            El recurso <a href="https://learngitbranching.js.org/?locale=es_ES">learngitbranching</a> permite aprender de manera fácil e incremental todos los conceptos y comandos de Git en profundidad, a través juegos de comandos por consola.
          </h3>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: two-cols
class: text-center p-12
transition: slide-up
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">GitHub</span>

<section>
    <div class="m-2 w-full  bg-white bg-opacity-20 rounded-xl p-2 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h3 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            GitHub es una plataforma en la nube que permite almacenar, compartir y colaborar en proyectos
            de código usando Git, facilitando el seguimiento y la gestión de cambios a lo largo del tiempo,
            y promoviendo el trabajo colaborativo entre desarrolladores.
          </h3>
        </div>
    </div>
</section>

::right::

<div class="flex fade-in items-center justify-center h-full">
  <img class="h-60" src="/github.png" alt="github" />
</div>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-left
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Facilidades de GitHub</span>

<section>
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
            <div class="space-y-6 text-lg font-semibold leading-relaxed drop-shadow-md list-none">
                  <v-click><p>🤖 Con GitHub Actions puedes automatizar la compilación y ejecución de pruebas cada vez que se hacen cambios en el repositorio, detectando errores rápidamente y asegurando la calidad del código antes de integrarlo.</p></v-click>
                  <v-click><p>🚀 Permite configurar flujos de trabajo que despliegan automáticamente las aplicaciones tras pasar las pruebas, facilitando la entrega continua y reduciendo errores manuales.</p></v-click>
                  <v-click><p>🧪 Los flujos de trabajo pueden incluir pruebas unitarias, funcionales y análisis estático de código para validar el software en cada cambio.</p></v-click>
                  <v-click><p>👥 GitHub facilita el control de versiones, revisión de código mediante pull requests, gestión de ramas y colaboración entre equipos, todo integrado en la plataforma.</p></v-click>
            </div>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: two-cols
class: text-center p-12
transition: slide-up
---

# <span class="text-4xl fade-in text-center font-extrabold drop-shadow-lg">Caso de estudio</span>

<section>
    <div class="m-6 w-full  bg-white bg-opacity-20 rounded-xl p-6 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h3 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Aplicación web instalable para el análisis en tiempo real de las tasas de cambio de divisas en el mercado informal cubano, con tecnología de elToque.
            <br>
            Disponible en <br> <a href="https://tasas-cuba.vercel.app">tasas-cuba.vercel.app</a>
          </h3>
        </div>
    </div>
</section>

::right::

<div class="flex fade-in items-center justify-center h-full">
  <img class="h-60" src="/tasas-cuba.png" alt="tasas-cuba" />
</div>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-up
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Commits y Branching</span>

<section class="flex items-center justify-center">
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
            <img class="h-80" src="/tc-repo.png" alt="repo"/>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-up
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Despliegues Automatizados</span>

<section class="flex items-center justify-center">
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
            <img class="h-80" src="/tc-deploy.png" alt="repo"/>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center p-12
transition: slide-left
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">Pruebas Automatizadas</span>

<section class="flex items-center justify-center">
    <div class="m-8 max-w-3xl mx-auto bg-white bg-opacity-20 rounded-xl p-8 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
            <img class="h-80" src="/tc-tests.png" alt="repo"/>
        </div>
    </div>
</section>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: two-cols
class: text-center p-12
transition: slide-left
---

<div class="flex fade-in items-center justify-center h-full">
  <img class="h-90" src="/slidev.png" alt="slidev" />
</div>

::right::

<section class="flex fade-in items-center justify-center h-full">
    <div class="m-6 w-full max-w-4xl bg-white bg-opacity-20 rounded-xl p-6 shadow-2xl">
        <div 
          v-motion 
          :initial="{ opacity: 0, scale: 0.85, y: 20 }" 
          :enter="{ opacity: 1, scale: 1, y: 0, transition: { delay: 150, duration: 600, ease: 'easeOut' } }"
        >
          <h3 class="text-2xl font-semibold leading-relaxed drop-shadow-md">
            Powered by <a href="https://sli.dev">sli.dev</a> y <a href="https://vuejs.org">Vue</a>
          </h3>
          <h3 class="text-2xl  leading-relaxed drop-shadow-md">
            Disponible en <br> <a href="https://vcs-jce.netlify.app/">vcs-presentation.netlify.app</a>
          </h3>
        </div>
    </div>
</section>


<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center
transition: slide-left
---

# <span class="text-6xl fade-in font-extrabold drop-shadow-lg">¿Preguntas y/o Comentarios?</span>

<style>
    .fade-in {
      animation: fadeIn 0.5s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
</style>

---
layout: center
class: text-center
transition: slide-left
---
<div class="background-container"></div>

# <span class="fade-in">Gracias por su atención</span>

<div class="text-slate-100 abs-br m-6 text-xl fade-in flex space-x-4">
  <a href="https://github.com/EduardoProfe666/vcs-presentation" target="_blank" class="slidev-icon-btn" aria-label="Código fuente presentación GitHub">
    <carbon:logo-github />
  </a>
  <a href="https://tasas-cuba.vercel.app/" target="_blank" class="slidev-icon-btn" aria-label="Ir a la aplicación tasas-cuba">
    <carbon:app />
  </a>

  <a href="https://github.com/EduardoProfe666/tasas-cuba" target="_blank" class="slidev-icon-btn" aria-label="Código fuente de la aplicación tasas-cuba en GitHub">
    <carbon:kubernetes-pod />
  </a>
</div>

<footer style="color: #05d8f3; font-weight: bold;" class="fade-in abs-b m-6">
  <a href="https://eduardoprofe666.github.io" target="_blank">Ing. Eduardo Alejandro González Martell</a>
</footer>

<style>
  .background-container {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url('/banner-final.webp');
    background-size: cover;
    background-position: center;
    filter: blur(8px);
    z-index: -1;
  }

  .fade-in {
      animation: fadeIn 1s ease-in-out forwards;
    }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  span {
    background-color: #81dbff;
    background-image: linear-gradient(45deg, #89effd 20%, #46c0ed 50%);
    background-size: 100%;
    -webkit-background-clip: text;
    -moz-background-clip: text;
    -webkit-text-fill-color: transparent;
    -moz-text-fill-color: transparent;
    font-weight: bold;
  }
</style>