<template>
  <div
    class="w-full bg-white border rounded-lg overflow-hidden card-producto border"
  >
    <div class="card-producto__header">
      <div class="w-full pb-2/3 relative bg-gray-400">
        <img
          class="absolute top-0 w-full h-full object-cover"
          src="~/assets/img/carnivoras.png"
          alt="Las carnivoras"
        />
      </div>
    </div>
    <div class="p-4 card-producto__body">
      <div class="card-producto__contenido">
        <h3
          class="mt-1 font-semibold text-lg leading-tight truncate card-producto__nombre"
        >
          Las Carnivoras
        </h3>
        <p class="mt-1 text-gray-600 text-sm card-producto__descripcion">
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sunt autem
          exercitationem, temporibus enim dolorem quasi unde quis est laborum,
          iste similique voluptates possimus incidunt sint dolores architecto.
          Dicta, laboriosam consequatur.
        </p>
      </div>
      <div class="mt-2 card-producto__footer">
        <button
          class="rounded py-2 px-4 bg-gray-500 hover:bg-gray-700 text-gray-100"
        >
          Añadir
        </button>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({})
</script>

<style>
</style>