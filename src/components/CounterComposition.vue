<!-- COMPOSITION API -->
<!-- //Este ejercicio se ha realizado con la intención de ejemplificar el COMPOSITION API -->
<template>
    <h3>{{ counter }}</h3>
    <button @click="addCounter">Incrementar</button>
</template>

<script lang="ts">
    import { defineComponent, Ref, ref } from 'vue'; //'ref' es para que refresque los cambios e indicar que es una referencia y queremos que Vue lo modifique
    export default defineComponent({
        name: 'CounterComposition',
        setup(){ //Lo que se genera dentro no es reactivo
            let counter:Ref = ref(0); //Indicamos que es una referencia y que se inicia en 0, con el 'Ref' indicamos que 'counter' es de tipo Ref.
            const addCounter = ():void => { //Con :void indicamos que la función devuelve un void(vacío).
                counter.value++; //Para utilizar una referencia debemos usar la propiedad 'value'
            }
            return {counter, addCounter};
        }
    })
</script>

<style scoped>

</style>