<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header class=" bg-[#a855f7]">
    
    <div class="wrapper">
      <nav >
    <div class="max-w-screen-xl px-4 py-3 mx-auto md:px-6">
        <div class="flex items-center">
            <ul class="flex flex-row mt-0 mr-6 space-x-8 text-sm font-medium ">
                <li class="hover:-translate-y-1 hover:scale-110 duration-300 hover:text-cyan-900">
                  <RouterLink to="/">Inicio</RouterLink> 
                </li>
                <li class="hover:-translate-y-1 hover:scale-110 duration-300 hover:text-cyan-900">
                  <RouterLink to="/about">Registro</RouterLink>
                    
                </li>
                <li class="hover:-translate-y-1 hover:scale-110 duration-300 hover:text-cyan-900">
                  <RouterLink to="/personajes">Informacion</RouterLink>
                </li>
            </ul>
        </div>
    </div>
</nav>
      

   
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
