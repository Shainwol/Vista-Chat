<template>
    <div class="card">
        <header>
            <span class="material-icons">account_circle</span>
            <h2>Nombre de Usuario</h2>
        </header>
        <p>Ultimo mensaje enviado</p>
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
        border-style: solid;
        border-color: beige;
        box-shadow: 0px 3px 8px lightcoral;
    }
</style>

<script setup lang="ts">

</script>