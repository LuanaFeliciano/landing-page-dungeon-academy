<template>
  <q-page-container>
    <q-page class="q-pa-md flex">
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
        <h1 class="q-mt-lg text-h3 text-dark">Dungeon Academy</h1>

        <!-- Subtítulo Persuasivo -->
        <h2 class="q-mt-md text-h5 text-dark">
          Desafie sua mente e vença os monstros!
        </h2>

        <!-- Descrição -->
        <div class="description q-mt-md q-pa-md">
          <p style="color: black">
            Dungeon Academy é um jogo educativo desenvolvido no GameMaker que
            proporciona uma experiência de aprendizado única. Ao invés de lutar,
            você deve responder a perguntas desafiadoras para derrotar monstros
            e progredir na história. Prepare-se para testar seu conhecimento e
            habilidades!
          </p>
        </div>

        <!-- Prova Social -->
        <div class="text-dark social-proof q-mt-md q-pa-md">
          <h3 class="text-h6 text-dark-blue">O que nossos jogadores dizem:</h3>
          <p class="quote">
            "Dungeon Academy é incrível! Aprendi muito enquanto me divertia!"
            <br />- Maria, Estudante
          </p>
          <p class="quote">
            "Um jogo desafiador que realmente estimula o cérebro!"
            <br />- João, Professor
          </p>
        </div>

        <!-- Benefícios e Proposta de Valor -->
        <div class="benefits q-mt-md q-pa-md">
          <h3 class="text-h6">Benefícios:</h3>
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
          @Click="goToGithub"
          :style="{ width: '100%', maxWidth: '200px' }"
        />
      </div>
    </q-page>
  </q-page-container>
</template>

<script setup>
function goToGithub() {
  window.open('https://github.com/LuanaFeliciano/DungeonAcademy', '_blank');
}
</script>
