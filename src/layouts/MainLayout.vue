<template>
  <q-layout view="lHh Lpr lFf" class="bg-light-grey">
    <!-- Header -->
    <q-header elevated class="bg-dark-blue text-white">
      <q-toolbar>
        <q-toolbar-title class="text-h5">Dungeon Academy</q-toolbar-title>
        <q-btn flat label="Início" @click="goHome" class="q-ml-sm text-white" />
        <q-btn flat label="about" to="/sobre" class="q-ml-sm" />
        <q-btn flat label="Contato" @click="goContact" class="q-ml-sm text-white" />
      </q-toolbar>
    </q-header>

    <!-- Conteúdo da página -->
    <q-page-container>
      <q-page class="q-pa-md flex flex-center">
        <div class="landing-container text-center">
          <!-- Logo -->
          <div class="logo-container">
            <img
              src="/src/assets/logo.png"
              alt="Dungeon Academy Logo"
              class="logo"
            />
          </div>

          <!-- Título -->
          <h1 class="q-mt-lg text-h3 text-dark-blue">Dungeon Academy</h1>

          <!-- Subtítulo Persuasivo -->
          <h2 class="q-mt-md text-h5 text-dark-grey">Desafie sua mente e vença os monstros!</h2>

          <!-- Descrição -->
          <div class="description q-mt-md q-pa-md">
            <p>
              Dungeon Academy é um jogo educativo desenvolvido no GameMaker que
              proporciona uma experiência de aprendizado única. Ao invés de lutar, você
              deve responder a perguntas desafiadoras para derrotar monstros e
              progredir na história. Prepare-se para testar seu conhecimento e
              habilidades!
            </p>
          </div>

          <!-- Prova Social -->
          <div class="social-proof q-mt-md q-pa-md">
            <h3 class="text-h6 text-dark-blue">O que nossos jogadores dizem:</h3>
            <p class="quote">
              "Dungeon Academy é incrível! Aprendi muito enquanto me divertia!"
              <br/>- Maria, Estudante
            </p>
            <p class="quote">
              "Um jogo desafiador que realmente estimula o cérebro!"
              <br/>- João, Professor
            </p>
          </div>

          <!-- Benefícios e Proposta de Valor -->
          <div class="benefits q-mt-md q-pa-md">
            <h3 class="text-h6 text-dark-blue">Benefícios:</h3>
            <ul class="benefit-list">
              <p>Desenvolva suas habilidades de raciocínio lógico.</p>
              <p>Aprimore seu conhecimento em várias áreas.</p>
              <p>Divirta-se enquanto aprende!</p>
              <p>Ideal para instituições de ensino e aprendizado colaborativo.</p>
            </ul>
          </div>

          <!-- Botão de Ação -->
          <q-btn
            class="q-mt-lg"
            label="Jogar Agora"
            color="dark-blue"
            @click="startGame"
            :style="{ width: '100%', maxWidth: '200px' }"
          />
        </div>
      </q-page>
    </q-page-container>

    <!-- Rodapé -->
    <q-footer class="bg-dark-blue text-white q-pa-md">
      <div class="text-center">
        <p>© 2024 Dungeon Academy. Todos os direitos reservados.</p>
        <p>
          <a href="#" class="text-white">Política de Privacidade</a> |
          <a href="#" class="text-white">Termos de Uso</a>
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

function startGame() {
  // Ação para iniciar o jogo
  router.push('/game-start');
}
</script>

<style scoped>
/* Cor de fundo suave */
.bg-light-grey {
  background-color: #f0f4f8;
}

/* Cores e estilos do Header */
.bg-dark-blue {
  background-color: #4262a5; /* Azul escuro */
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

/* Estilo da logo */
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

/* Seções com bordas suaves e sombras */
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

/* Botão */
.q-btn {
  background-color:  #171421; /* Azul escuro */
  color: #fff; /* Texto do botão em branco */
}

/* Estilo do rodapé */
.q-footer {
  background-color: #4262a5;
}

/* Media Queries para ajustar a responsividade em telas menores */
@media (max-width: 600px) {
  .landing-container {
    padding: 10px;
  }
}
</style>
