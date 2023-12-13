<template>
    <div class="contenedormensajeder">
        <div class="mensajeder">{{ mensaje }}</div>
    </div>
</template>

<style>
    .contenedormensajeder{
        width: 100%;
        display: flex;
        justify-content: end;
    }
    .mensajeder{
        max-width: fit-content;
        padding: 5px;
        margin: 5px;
        background-color: beige;
        color:lightcoral;
        border-radius: 15px 15px 0 15px;
        min-width: 50px;
        display: flex;
        justify-content: end;
    }
</style>

<script setup lang="ts">
    defineProps<{
    mensaje: string
    }>()
</script>