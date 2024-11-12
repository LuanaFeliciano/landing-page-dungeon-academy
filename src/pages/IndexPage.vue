<template>
  <q-page-container>
    <q-page class="q-pa-sm flex">
      <div class="landing-container text-center">
        <!-- Logo -->
        <div class="logo-container">
          <img
            src="/src/assets/logo.png"
            alt="Dungeon Academy Logo"
            class="logo"
          />
        </div>

        <h2 class="q-mt-md text-h2 text-weight-bold">
          Desafie sua mente e vença os monstros!
        </h2>

        <div class="row description q-mt-lg q-pa-sm">
          <div class="col-2 q-pl-lg">
            <q-img
              src="/src/assets/cheirado.png"
              class="items-start"
              style="height: 310px; width: 300px"
            />
          </div>
          <div class="col-9 q-pa-lg">
            <h4
              class="q-pa-lg text-justify text-weight-medium"
              style="color: black"
            >
              Dungeon Academy é um jogo educativo desenvolvido no GameMaker que
              proporciona uma experiência de aprendizado única. Ao invés de
              lutar, você deve responder a perguntas desafiadoras para derrotar
              monstros e progredir na história. Prepare-se para testar seu
              conhecimento e habilidades!
            </h4>
          </div>
        </div>

        <div class="row description q-mt-lg q-pa-sm">
          <div class="col-9 q-pa-lg">
            <h4
              class="q-pa-lg text-justify text-weight-medium"
              style="color: black"
            >
              Unindo elementos de jogos RPG, com a temática medieval e também
              mesclando elementos modernos, Dungeon Academy tem como seu
              principal foco alunos de ensino fundamental/médio, com o intuito
              de despertar o conhecimento dos jogadores, além de garantir que o
              aprendizado seja de forma leve e divertida.
            </h4>
          </div>
          <div class="col-2">
            <q-img
              src="/src/assets/cheirado.png"
              class="items-start"
              style="height: 310px; width: 300px"
            />
          </div>
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
