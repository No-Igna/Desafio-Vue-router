<template>
  <div class="container mt-5 pt-5">
    <h1>Página de Contacto</h1>
    <p>Bueno, esta pagina se encuentra un poco vacia ya que no se especifico que debia contener, solo tenia que exisitr, por favor, precionar el boton "ir a inicio" para volver al inicio si asi lo desea.</p>
    <button type="button" class="btn btn-secondary my-2" @click="goHome">Ir a Inicio</button>
  </div>
</template>

<script>
export default {
  name: 'Contacto',
  methods: {
    goHome() {
      this.$router.push("/");
    },
  },
};
</script>