<template>
  <q-layout view="lHh Lpr lFf" class="bg-light-grey">
    <!-- Header -->
    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <!-- Logo ou título -->
        <q-toolbar-title class="text-h5"> Dungeon Academy </q-toolbar-title>

        <!-- Botões de navegação -->
        <q-btn flat label="Início" @click="goHome" class="q-ml-sm text-white" />
        <q-btn flat label="Sobre" @click="goAbout" class="q-ml-sm text-white" />
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
              src="src/assets/logo.png"
              alt="Dungeon Academy Logo"
              class="logo"
            />
          </div>

          <!-- Título -->
          <h1 class="q-mt-lg text-h3 text-primary">Dungeon Academy</h1>

          <!-- Subtítulo Persuasivo -->
          <h2 class="q-mt-md text-h5 text-grey-8">Desafie sua mente e vença os monstros!</h2>

          <!-- Descrição -->
          <div class="description q-mt-md q-pa-md">
            <p>
              Você acordou em uma Dungeon e descobre monstros ao seu redor,
              porém, eles não o atacam fisicamente. Eles o desafiam com questões
              e perguntas, e você é obrigado a vencê-los usando sua
              inteligência. Sua maior arma é o conhecimento!
            </p>
          </div>

          <!-- Prova Social -->
          <div class="social-proof q-mt-md q-pa-md">
            <h3 class="text-h6">O que nossos jogadores dizem:</h3>
            <p class="quote">
              "Dungeon Academy é incrível! Aprendi muito enquanto me divertia!"
              <br/>- Jogador satisfeito
            </p>
            <p class="quote">
              "Um jogo desafiador que realmente estimula o cérebro!"
              <br/>- Jogador entusiasmado
            </p>
          </div>

          <!-- Benefícios e Proposta de Valor -->
          <div class="benefits q-mt-md q-pa-md">
            <h3 class="text-h6">Benefícios:</h3>
            <ul class="benefit-list">
              <p>Desenvolva suas habilidades de raciocínio lógico.</p>
              <p>Aprimore seu conhecimento em várias áreas.</p>
              <p>Divirta-se enquanto aprende!</p>
            </ul>
          </div>

          <!-- Botão de Ação -->
          <q-btn
            class="q-mt-lg"
            label="Jogar Agora"
            color="primary"
            @click="startGame"
            :style="{ width: '100%', maxWidth: '200px' }"
          />
        </div>
      </q-page>
    </q-page-container>

    <!-- Rodapé -->
    <q-footer class="bg-grey-9 text-white q-pa-md">
      <div class="text-center">
        <p>© 2024 Dungeon Academy. Todos os direitos reservados.</p>
        <p>
          <a href="#" class="text-white">Política de Privacidade</a> |
          <a href="#" class="text-white">Termos de Uso</a>
        </p>
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

function goAbout() {
  router.push('/about');
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
.bg-light-grey {
  background-color: #f0f4f8; /* Cor de fundo mais suave */
}

.q-toolbar-title {
  font-weight: bold;
}

.landing-container {
  max-width: 600px;
  width: 100%;
  margin: 0 auto;
  padding: 20px; /* Adiciona espaço interno */
  background: white; /* Fundo branco para o contêiner */
  border-radius: 15px; /* Bordas arredondadas */
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1); /* Sombra para profundidade */
}

.logo-container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px; /* Espaço abaixo do logo */
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
  padding: 15px; /* Padding interno para as seções */
}

.quote {
  font-style: italic;
  color: #555; /* Cor cinza para as citações */
}

.benefit-list {
  list-style-type: disc; /* Estilo de lista para benefícios */
  padding-left: 20px; /* Indentação para lista */
}

.q-footer {
  background-color: #2c2c2c;
}

/* Media Queries para ajustar a responsividade em telas menores */
@media (max-width: 600px) {
  .landing-container {
    padding: 10px; /* Aumenta o padding em telas pequenas */
  }
}
</style>
