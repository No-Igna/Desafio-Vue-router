<template lang="">
  <div class="col-4 p-2">
    <div class="card">
      <img :src="producto.imagen" class="card-img-top" :alt="producto.nombre" />
      <div class="card-body">
        <h5 class="card-title fw-bold">{{ producto.nombre }}</h5>
        <p class="card-text">
          {{ producto.descripcion }}
        </p>
      </div>
      <ul class="list-group list-group-flush">
        <li class="list-group-item">Precio: {{ producto.precio }}</li>
        <li class="list-group-item">Cantidad: {{ producto.cantidad }}</li>
      </ul>
      <div class="card-body">
        <a href="#" class="card-link">Ver más</a>
        <a href="#" class="card-link">Comprar</a>
      </div>
    </div>
  </div>

</template>
<script>
export default {
  props: {
    producto: Object
  }

}
</script>
<style lang="">

</style>