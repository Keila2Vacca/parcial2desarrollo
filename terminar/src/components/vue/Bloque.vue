
<script setup>
import { ref } from 'vue';

const temas = ref([
  { id: 1, titulo: "Tema 1", info: "Información del Tema 1", visible: false },
  { id: 2, titulo: "Tema 2", info: "Información del Tema 2", visible: false },
  { id: 3, titulo: "Tema 3", info: "Información del Tema 3", visible: false },
  { id: 4, titulo: "Tema 4", info: "Información del Tema 4", visible: false },
]);

function toggleInfo(index) {
  if (temas.value[index]) {
    temas.value[index].visible = !temas.value[index].visible; 
  }
}
</script>

<template>
  <div class="bg-blue-400 w-96 flex flex-col items-center">
    <div
      v-for="(tema, index) in temas"
      :key="tema.id"
      class="w-full flex flex-col items-center mb-4"
    >
      <div class="mt-4 mb-4 flex justify-between w-3/4 bg-blue-100 p-2 rounded-md">
        <div class="font-semibold text-14px text-blue-600">{{ tema.titulo }}</div>
        <button @click="toggleInfo(index)" class="w-10">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" style="fill: blue;">
            <path d="M19 11h-6V5h-2v6H5v2h6v6h2v-6h6z"></path>
          </svg>
        </button>
      </div>
      
      <div
        v-show="tema.visible"
        class="bg-white text-blue-600 w-3/4 p-2 rounded-md"
      >
        {{ tema.info }}
      </div>
    </div>
  </div>
</template>
