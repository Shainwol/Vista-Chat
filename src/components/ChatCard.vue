<template>
    <div class="card">
        <span class="material-icons">
account_circle
</span>
        <h2>Nombre de Usuario</h2>
        <p>Ultimo mensaje enviado</p>
    </div>
</template>

<style>
    h2{
        font-size: 16px;
    }
    .card{
        background-color: beige;
        padding: 5px;
        margin-top: 5px;
        border-radius: 10px;
    }
    .card:hover{
        background-color: white;
        transform: translateY(-3px);
        border-style: solid;
        border-color: beige;
    }
</style>

<script setup lang="ts">

</script>