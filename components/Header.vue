<template>
  <div>
    <header class="w-full fixed top-0 z-50 bg-gray-800">
      <div
        class="container flex items-center justify-between mx-auto px-4 py-2"
      >
        <div class="text-gray-200">Logo</div>
        <button @click="isOpen = !isOpen">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 448 512"
            class="h-6 w-6 fill-current text-gray-200"
          >
            <path
              v-if="!isOpen"
              d="M436 124H12c-6.627 0-12-5.373-12-12V80c0-6.627 5.373-12 12-12h424c6.627 0 12 5.373 12 12v32c0 6.627-5.373 12-12 12zm0 160H12c-6.627 0-12-5.373-12-12v-32c0-6.627 5.373-12 12-12h424c6.627 0 12 5.373 12 12v32c0 6.627-5.373 12-12 12zm0 160H12c-6.627 0-12-5.373-12-12v-32c0-6.627 5.373-12 12-12h424c6.627 0 12 5.373 12 12v32c0 6.627-5.373 12-12 12z"
            ></path>
            <path
              v-else
              d="M207.6 256l107.72-107.72c6.23-6.23 6.23-16.34 0-22.58l-25.03-25.03c-6.23-6.23-16.34-6.23-22.58 0L160 208.4 52.28 100.68c-6.23-6.23-16.34-6.23-22.58 0L4.68 125.7c-6.23 6.23-6.23 16.34 0 22.58L112.4 256 4.68 363.72c-6.23 6.23-6.23 16.34 0 22.58l25.03 25.03c6.23 6.23 16.34 6.23 22.58 0L160 303.6l107.72 107.72c6.23 6.23 16.34 6.23 22.58 0l25.03-25.03c6.23-6.23 6.23-16.34 0-22.58L207.6 256z"
            ></path>
          </svg>
        </button>
      </div>
      <div v-if="isOpen" class="w-full fixed z-50 top-10 h-screen">
        <div class="w-2/3 ml-auto h-100 bg-gray-800 h-full overflow-auto">
          <nav class="overflow-y-hidden">
            <a
              href="#"
              class="text-white block px-2 mx-2 mb-1 rounded hover:bg-gray-600"
              >Menu</a
            >
            <a
              href="#"
              class="text-white block px-2 mx-2 mb-1 rounded hover:bg-gray-600"
              >Locales</a
            >
            <a
              href="#"
              class="text-white block px-2 mx-2 mb-1 rounded hover:bg-gray-600"
              >Ingresar</a
            >
            <a
              href="#"
              class="text-white block px-2 mx-2 mb-1 rounded hover:bg-gray-600"
              >Carrito</a
            >
          </nav>
        </div>
      </div>
    </header>
    <div
      v-if="isOpen"
      class="w-screen h-screen fixed top-0 bg-gray-200 opacity-75 z-30"
    ></div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      isOpen: false,
    }
  },
})
</script>

<style>
</style>