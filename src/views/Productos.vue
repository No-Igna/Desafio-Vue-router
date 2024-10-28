<script>
import Card from '../components/Card.vue'

export default {
  components: {
    Card
  },
  data() {
    return {
      productos: [
        {
          nombre: "Bebidas",
          descripcion: "Refrescos naturales y jugos frescos para acompañar tus comidas.",
          precio: "$1,500",
          cantidad: "Botella de 500 ml", imagen: "./src/assets/img/bebidas.jpg"
        },
        {
          nombre: "Colaciones",
          descripcion: "Snack saludables y energéticos perfectos para cualquier momento del día.",
          precio: "$800",
          cantidad: "Porción de 100 g", 
          imagen: "./src/assets/img/colaciones.jpg"
        },
        {
          nombre: "Desayunos",
          descripcion: "Nutritivos y deliciosos desayunos ideales para comenzar el día con energía.",
          precio: "$2,000",
          cantidad: "Para dos personas", 
          imagen: "./src/assets/img/desayunos.jpg"
        },
        {
          nombre: "Dulces",
          descripcion: "Exquisitos postres y golosinas para satisfacer tu antojo dulce.",
          precio: "$1,200",
          cantidad: "Caja de 6 piezas", 
          imagen: "./src/assets/img/dulces.jpg"
        },
        {
          nombre: "Empanadas",
          descripcion: "Empanadas frescas y crujientes, rellenas de ingredientes variados y deliciosos.",
          precio: "$2,500",
          cantidad: "Paquete de 4 empanadas", 
          imagen: "./src/assets/img/empanadas.jpg"
        },
        {
          nombre: "Verduras",
          descripcion: "Verduras frescas y de calidad, ideales para ensaladas y acompañamientos saludables.",
          precio: "$1,000",
          cantidad: "Bolsa de 500 g",
          imagen: "./src/assets/img/verduras.jpg"
        },
      ],
    };
  },
  methods: {
    goHome() {
      this.$router.push("/");
    },
  },
}
</script>

<template>
  <section class="container" id="productos">
    <div class="col-12 mb-4">
      <h1 class=" text-center">Nuestros Productos</h1>
      <div class="row">
        <Card v-for="producto in productos" :key="producto.nombre" :producto="producto" />
      </div>
    </div>
    <button type="button" class="btn btn-secondary my-2" @click="goHome">Ir a Inicio</button>
  </section>
</template>
