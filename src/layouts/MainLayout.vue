<template>
  <q-layout view="lHh Lpr lFf" class="bg-light-grey">
    <q-header elevated class="bg-dark-blue text-white">
      <q-toolbar>
        <q-toolbar-title class="text-h5">Dungeon Academy</q-toolbar-title>
        <q-btn flat label="Início" @click="goHome" class="q-ml-sm text-white" />
        <q-btn flat label="Contato" @click="goContact" class="q-ml-sm text-white" />
      </q-toolbar>
    </q-header>
    <q-page-container>
      <router-view /> <!-- Aqui as páginas como IndexPage serão renderizadas -->
    </q-page-container>
    <q-footer class="bg-dark-blue text-white q-pb-sm q-mt-xs">
      <div class="q-mt-xs text-center text-caption">
        <p>© 2024 Dungeon Academy. Todos os direitos reservados.</p>
        <p>
          <a href="#" class="text-white ">Política de Privacidade</a> |
          <a href="#" class="text-white ">Termos de Uso</a>
        </p>
        <p>Contato: <a href="mailto:contato@dungeonacademy.com" class="text-white">contato@dungeonacademy.com</a></p>
      </div>
    </q-footer>
  </q-layout>
</template>

<script setup lang="ts">
import { useRouter } from 'vue-router';

const router = useRouter();

function goHome() {
  router.push('/');
}

function goContact() {
  router.push('/contact');
}


</script>

<style scoped>

.bg-light-grey {
  background-color: #f0f4f8;
}

.bg-dark-blue {
  background-color: #4262a5;
}

.text-dark-blue {
  color: #002e6d;
}

.text-dark-grey {
  color: #4a4a4a;
}

.landing-container {
  max-width: 600px;
  width: 100%;
  margin: 0 auto;
  padding: 20px;
  background: white;
  border-radius: 15px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.logo-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;
}

.logo {
  width: 100%;
  max-width: 200px;
  height: auto;
  border-radius: 50%;
}

.description, .social-proof, .benefits {
  background-color: #f5f5f5;
  border-radius: 10px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  padding: 15px;
}

.quote {
  font-style: italic;
  color: #555;
}

.benefit-list {
  list-style-type: disc;
  padding-left: 20px;
}

.q-btn {
  background-color:  #171421;
  color: #fff;
}

.q-footer {
  background-color: #4262a5;
}

@media (max-width: 600px) {
  .landing-container {
    padding: 10px;
  }
}
</style>
