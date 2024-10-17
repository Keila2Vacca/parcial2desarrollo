<script setup>
import { ref } from 'vue';
const info = ref("información del tema");
const status = ref(false);
function show() {
    status.value == !status.value;
}
</script>

<template>
    <div class="bg-blue-400 w-96 flex flex-col items-center">

        <div class="mt-4 mb-4 flex justify-between w-3/4 bg-blue-100">
            <div class=" font-semibold text-14px p-18px text-blue-600">Tema 1</div>
            <button @click="show" class="w-10" > 
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"
                    style="fill: blue-600">
                    <path d="M19 11h-6V5h-2v6H5v2h6v6h2v-6h6z"></path>
                </svg>
            </button>
        </div>
        <div v-show="status" class="bg-white size-12 text-blue-600 w-3/4 ">
            {{ info }}
        </div>
        <div class="mt-4 mb-4 flex justify-between w-3/4 bg-blue-100">
            <div class=" font-semibold text-14px p-18px text-blue-600">Tema 2</div>
            <button @click="show" class="w-10">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"
                    style="fill: blue-600">
                    <path d="M19 11h-6V5h-2v6H5v2h6v6h2v-6h6z"></path>
                </svg>
            </button>
        </div>
        <div v-show="status" class="bg-white size-12 text-blue-600 w-3/4 ">
            {{ info }}
        </div>
        <div class="mt-4 mb-4 flex justify-between w-3/4 bg-blue-100">
            <div class=" font-semibold text-14px p-18px text-blue-600">Tema 3</div>
            <button @click="show" class="w-10">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"
                    style="fill: blue-600">
                    <path d="M19 11h-6V5h-2v6H5v2h6v6h2v-6h6z"></path>
                </svg>
            </button>
        </div>
        <div v-show="status" class="bg-white size-12 text-blue-600 w-3/4 ">
            {{ info }}
        </div>
        <div class="mt-4 mb-4 flex justify-between w-3/4 bg-blue-100">
            <div class=" font-semibold text-14px p-18px text-blue-600">Tema 4</div>
            <button @click="show" class="w-10">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"
                    style="fill: blue-600">
                    <path d="M19 11h-6V5h-2v6H5v2h6v6h2v-6h6z"></path>
                </svg>
            </button>
        </div>
        <div v-show="status" class="bg-white size-12 text-blue-600 w-3/4 mb-4 ">
            {{ info }}
        </div>

    </div>
</template>