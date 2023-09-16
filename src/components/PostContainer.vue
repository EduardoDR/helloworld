<template>
    <div class="post-container">
        <PostCard/>
        <PostCard/>
        <PostCard/>
        <PostCard/>
    </div>
</template>

<script lang="ts" setup>
    /* Importamos el componente creado anteriormente que también hace referencia a otro componente (PostButton.vue) */
    import PostCard from './PostCard.vue'
</script>

<style>
    .post-container{
        width: 100%;
        display: flex;
        flex-wrap: wrap;
    }
</style>