<template>
  <div class="container mx-auto mt-14 px-4">
    <div
      class="w-full grid grid-cols-1 gap-4 sm:grid-cols-2 lg:grid-cols-3 row-productos"
    >
      <CardProducto
        v-for="producto in productos"
        :key="producto.id"
      ></CardProducto>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

interface Producto {
  id: number
  nombre: string
}

export default Vue.extend({
  data() {
    return {
      productos: new Array<Producto>(),
    }
  },
  created() {
    this.fetchProductos()
  },
  fetch() {},
  methods: {
    fetchProductos() {
      this.$axios
        .$get(`http://localhost:1337/productos`)
        .then((res: Array<Producto>) => {
          this.productos = res
          console.log(res)
        })
        .catch((err: any) => {
          console.log(err.response)
        })
    },
  },
})
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
</style>
