CONTRACT.md
Toda app vive en src/apps/<slug>/ y contiene exactamente estos 3 archivos:

meta.js

js
export default {
  name: '',          // 3–60 chars
  description: '',   // 10–160 chars
  category: '',      // texto|imagen|audio|video|datos|utilidades
  icon: '',          // emoji
  tags: [],          // opcional, máx 6
  order: 0,          // opcional
}
index.js

js
export default () => import('./App.vue')
App.vue

vue
<script setup>
// lógica
</script>
<template>
  <div class="app"><!-- UI --></div>
</template>
Reglas

slug = nombre de carpeta, kebab-case, minúsculas.

App.vue no importa de otras apps, no usa stores globales, no llama a red ni APIs.

Nunca tocar router, registry ni landing. La app se descubre sola.

Permitido dentro de la carpeta: lib/, assets/, *.wasm, README.md.

Respuesta obligatoria de la IA (siempre este formato):

text
1. Slug:
2. Categoría:
3. Archivos (uno por bloque con su ruta):
4. Modificar registro: ninguno
5. Verificación: npm run validate
6. Notas:
