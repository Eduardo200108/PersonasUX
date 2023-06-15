<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <WelcomeItem>
    <template #icon>
      <DocumentationIcon />
    </template>
    <template #heading>Bienvenido a personas Ux
    </template>

  <img class="w-24" src="/ux.jpg" alt="formulario ">
    <a href="https://vuejs.org/" target="_blank" rel="noopener">Proyecto unidad 1</a>
    
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <ToolingIcon />
    </template>
    <template #heading>¿que es personas ux?</template>
    Una UX Persona es un personaje ficticio que representa a tus usuarios objetivo. Las personas son una herramienta UX extremadamente valiosa, que permiten comprender mejor a tu público objetivo y, en consecuencia, tomar decisiones de diseño.
    
    <a href="https://vitejs.dev/guide/features.html" target="_blank" rel="noopener"></a>
    <a href="https://code.visualstudio.com/" target="_blank" rel="noopener"></a> 
    <a href="https://github.com/johnsoncodehk/volar" target="_blank" rel="noopener"></a>
    <a href="https://www.cypress.io/" target="_blank" rel="noopener"></a>
    <a href="https://on.cypress.io/component" target="_blank"></a>

    <br />

    <code></code>.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <EcosystemIcon />
    </template>
    <template #heading>¿Cuál es la importancia del diseño UX?</template>

    El diseño y la usabilidad de las páginas web son esenciales para que el cliente pueda tener una buena experiencia en ella. Esto se traduce en un buen diseño UX, algo en lo que toda aquella persona que quiere emprender un proyecto digital debe fijarse. A continuación te mostramos cuál es la importancia del diseño […]
    <a href="https://pinia.vuejs.org/" target="_blank" rel="noopener"></a>
    <a href="https://router.vuejs.org/" target="_blank" rel="noopener"></a>
    <a href="https://test-utils.vuejs.org/" target="_blank" rel="noopener"></a>
    <a href="https://github.com/vuejs/devtools" target="_blank" rel="noopener"></a>
    <a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener"></a>
    a visit.
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <CommunityIcon />
    </template>
    <template #heading></template>

   
    <a href="https://chat.vuejs.org" target="_blank" rel="noopener"></a>
    <a href="https://stackoverflow.com/questions/tagged/vue.js" target="_blank" rel="noopener"
      ></a
    >
    <a href="https://news.vuejs.org" target="_blank" rel="noopener"></a> 
    
    <a href="https://twitter.com/vuejs" target="_blank" rel="noopener"></a>
    
  </WelcomeItem>

  <WelcomeItem>
    <template #icon>
      <SupportIcon />
    </template>
    <template #heading></template>

    
    <a href="https://vuejs.org/sponsor/" target="_blank" rel="noopener"></a>.
  </WelcomeItem>
</template>
