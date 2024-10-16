<script setup>
import Counter from "../src/components/MIS COMPONENTES/Counter.vue";
</script>

<template>
  <header>
    <div class="container">
      <img
        alt="Vue logo"
        class="logo"
        src="@/assets/logo.svg"
        width="125"
        height="125"
      />
      <div class="counters">
        <Counter title="Entraron" />
        <Counter title="Salieron" :start="10" />
      </div>
    </div>
  </header>
</template>

<style scoped>
.container {
  max-width: 1200px; /* Ajusta según sea necesario */
  margin: 0 auto; /* Centra el contenedor */
  display: flex;
  flex-direction: column; /* Coloca los elementos uno encima del otro en pantallas pequeñas */
  align-items: center; /* Centra horizontalmente los elementos */
}

.logo {
  display: block;
  margin-bottom: 2rem; /* Espacio entre el logo y los contadores */
}

.counters {
  display: flex;
  justify-content: center; /* Centra los contadores horizontalmente */
}

header {
  text-align: center;
}

@media (min-width: 1000px) {
  .container {
    flex-direction: row; /* Cambia a fila en pantallas grandes */
    justify-content: center; /* Mantiene todo centrado */
    align-items: center; /* Alinea verticalmente al centro */
    padding-right: calc(var(--section-gap) / 2);
    padding-left: calc(
      var(--section-gap) / 2
    ); /* Agrega padding a la izquierda para mantenerlo centrado */
  }

  .logo {
    margin-right: 2rem; /* Espacio entre el logo y los contadores */
    margin-bottom: 0; /* Elimina el margen inferior en pantallas grandes */
  }
}
</style>
