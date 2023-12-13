<template>
<div class="card">
    <header>
        <span class="material-icons">account_circle</span>
        <h2>Nombre de Usuario</h2>
    </header>
    <p>Descripcion del contacto</p>
</div>
</template>

<style>
    header{
        display: flex;
        flex-direction: row;
    }
    h2{
        font-size: 16px;
    }
    .card{
        background-color: beige;
        padding: 5px;
        margin-top: 5px;
        border-radius: 10px;
        transition: all 0.15s ease-in-out;
    }
    .card:hover{
        background-color: white;
        transform: translateY(-3px);
        border-color: beige;
    }
</style>

<script setup lang="ts">

</script>