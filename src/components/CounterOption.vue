<!-- OPTION API -->
<!-- //Este ejercicio se ha realizado con la intención de ejemplificar el OPTION API -->
<template>
    <h3>{{ counter }}</h3>
    <button @click="addCounter">Incrementar</button>

</template>

<script lang="ts"> //Ya no vamos a utilizar el 'setup' por que vamos a hacer la construcción completa
    import { defineComponent } from 'vue';

    //Aquí se importan primero los componentes que se esten utilizando

    //Definimos el componente
    export default defineComponent({
        name: 'CounterOption',
        components: {}, //Aquí se definen todos los componentes que se esten utilizando, aunque primero hay que importarlos
        data(){//Contiene los datos que estará utilizando el componente: variables, elementos.
            let counter = 0;
            /* return {counter: 0} //Se puede retornar sin antes definir la variable, de esta manera */
            return {counter}
        },
        methods:{//Los métodos que tendrá mi componente
            //Método que va a incrementar
            addCounter(){
                this.counter++
            },//S i hay más métodos se agregan a continuación
        },
    })
</script>

<style scoped>

</style>