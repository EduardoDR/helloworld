<!-- El código HTML que va a contener nuestra aplicación -->
<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Hola mundo</h1>
  <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Ipsa tempore facilis laboriosam natus animi! Praesentium minima temporibus odit alias numquam, suscipit magnam doloribus optio est velit, veritatis soluta fugiat aut!</p>
  <CounterOption />
  <CounterComposition />
  <PostContainer />
  


</template>

<!-- La lógica de funcionamiento y los datos de dicho componente-->
<script lang="ts"> /* lang="ts", nos indica que estamos escribiendo en lenguaje TypeScript y no JavaScript */
import { defineComponent } from 'vue';

//Importamos los primeros componentes creados por mí :'v
import PostContainer from './components/PostContainer.vue';

//Importamos el componente: CounterOption (OPTION API)
import CounterOption from './components/CounterOption.vue';

//Importamos el componente: CounterComposition (COMPOSITION API)
import CounterComposition from './components/CounterComposition.vue';

export default defineComponent({
  name: 'App',
  components: {
    PostContainer, //Ya que en esta etiqueta script no la definí con la propiedad 'setup', me imaginé que aquí tendría que declarar el componente
    CounterOption,
    CounterComposition,
  }
});
</script>

<!-- El CSS que afecta al componente, tenemos 2 formatos de estilos "scoped" o hacerlos generales -->
<style> /* Entiendo que los 2 formatos es: definir estilos que afecten de manera global o afecten solo al componente */
h1 {
  color: green;
}
#app { /* Deduzco que este es un estilo que solo afecta el componente #app (scoped), para declararlo de manera global seria de colocarlo dentro de las etiquetas <style> */
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
