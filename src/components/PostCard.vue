<template>
    <div class="post-card">
        <h3>Título</h3>
        <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Consequuntur, eos delectus. Unde quo placeat blanditiis veritatis porro distinctio vitae dolores corrupti itaque veniam neque aspernatur, nesciunt corporis, temporibus, obcaecati at?</p>
        <PostButton/>
    </div>
</template>

<script lang="ts" setup>
    /* Importamos el componente (definido anteriormente), para poderlo utilizarlo en el template*/
    import PostButton from './PostButton.vue'
</script>

<style scoped>
.post-card{
    border-radius: 15px;
    padding: 10px;
    margin: 5px;
    border: 1px solid #ccc;
}
</style>