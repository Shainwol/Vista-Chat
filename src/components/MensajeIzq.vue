<template>
    <div class="contenedormensajeizq">
        <div class="mensajeizq">{{ mensaje }}</div>
    </div>
</template>

<style>
    .contenedormensajeizq{
        width: 100%;
        display: flex;
        justify-content: start;
    }
    .mensajeizq{
        max-width: fit-content;
        padding: 5px;
        margin: 5px;
        background-color: lightcoral;
        color:white;
        border-radius: 15px 15px 15px 0;
        min-width: 50px;
        display: flex;
        justify-content: start;
    }
</style>

<script setup lang="ts">
    defineProps<{
    mensaje?: string
    }>()
</script>