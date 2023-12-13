<template>
    <div class="d-flex contenedor">
        <div class="sidebar">
            <div class="buscador">
                <input type="text" placeholder="buscar">
                <span class="material-icons">search</span>
            </div>
            <h1>Chats</h1>
            <hr>
            <div class="chats">
                <ChatCard/>
                <ChatCard/>
                <ChatCard/>
            </div>
            <h1>Contactos</h1>
            <hr>
            <div class="contactos">
                <ContactCard/>
                <ContactCard/>
                <ContactCard/>
                <ContactCard/>
            </div>
        </div>
        
        <div class="chat">
            <header>
                <h1>Nombre de Usuario</h1>
                <span class="material-icons">call</span>
                <span class="material-icons">videocam</span>
                <span class="material-icons">search</span>
                <span class="material-icons">more_vert</span>
            </header>
            <hr>
            <div class="mensajes">
                
            </div>
            <div class="enviar-mensaje">
                <input type="text" placeholder="Enviar Mensaje">
                <button @click="enviar()">Enviar</button>
            </div>
        </div>
    </div>
    </template>
<style>
h1{
    font-size: 24px;
}
input{
    border: 3px;
    border-style: solid;
    border-color: lightcoral;
    border-radius: 10px;
    padding: 5px;
    margin-bottom: 15px;
}
.contenedor{
    position: fixed;
    top: 0px;
    bottom: 0px;
    left: 0px;
    right: 0px;
    margin: 0px;
    padding: 10px;
    color:lightcoral;
    background-color: beige;
}
.buscador{
    position: relative;
}
.buscador span{
    
}

.sidebar{
    background-color: white;
    margin: 0px;
    padding: 10px;
    border-radius: 15px;
}
.chats{
    max-height: 35%;
    overflow-y: scroll;
}
.contactos{
    max-height: 35%;
    overflow-y: scroll;
}

.chat{
    background-color: white;
    margin: 0px;
    margin-left: 10px;
    padding: 10px;
    width: 100%;
    display: flex;
    flex-direction:column;
}
.mensajes{
    height: 95%;
}

.enviar-mensaje{
    width: 100%;
    margin-top: 10px;
}

.enviar-mensaje input{
    
}

.chat .enviar-mensaje button{
    background-color: lightcoral;
    color: white;
    padding:10px;
    border-radius: 15px;
    padding: 8px;
    margin-left: 10px;
    min-width: 80px;
}

</style>

<script setup lang="ts">
  import ContactCard from './ContactCard.vue';
  import ChatCard from './ChatCard.vue'

  function enviar() {
    alert("Mensaje enviado")
  }
</script>