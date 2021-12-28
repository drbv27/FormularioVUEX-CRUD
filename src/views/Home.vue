<template>
  <h1 class="my-5">Formularios con Vue.js</h1>
  <form class="mt-3" @submit.prevent="procesarFormulario">
    <Input :tarea="tarea" />
  </form>
  <hr />
  <p>{{ tarea }}</p>
</template>

<script>
import Input from "../components/Input";

export default {
  name: "Home",
  components: {
    Input,
  },
  data() {
    return {
      tarea: {
        id: "",
        nombre: "",
        categorias: [],
        estado: "",
        numero: 0,
      },
    };
  },
  methods: {
    procesarFormulario() {
      console.log(this.tarea);
      if (this.tarea.nombre.trim() === "") {
        console.log("vacio");
        return;
      }
      console.log("No está vacio");
      //enviar los datos

      this.tarea = {
        nombre: "",
        categorias: [],
        estado: "",
        numero: 0,
      };
    },
  },
};
</script>
