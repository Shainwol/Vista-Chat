<template>
    <div class="d-flex contenedor">
        <div class="sidebar">
            <div class="buscador d-flex flex-row">
                <input type="text" placeholder="buscar">
                <span class="material-icons" @click="buscar()">search</span>
            </div>
            <div class="chatscontenedor">
                <h1>Chats</h1>
                <hr>
                <div class="chats">
                    <ChatCard/>
                    <ChatCard/>
                    <ChatCard/>
                </div>
            </div>
            <div class="contactoscontenedor">
                <h1>Contactos</h1>
                <hr>
                <div class="contactos">
                    <ContactCard/>
                    <ContactCard/>
                    <ContactCard/>
                    <ContactCard/>
                </div>
            </div>
        </div>
        
        <div class="chatbox">
            <header>
                <h1>Nombre de Usuario</h1>
                <div class="iconos">
                    <span class="material-icons" @click="llamar()">call</span>
                    <span class="material-icons" @click="videollamar()">videocam</span>
                    <span class="material-icons">search</span>
                    <span class="material-icons">more_vert</span>
                </div>
            </header>
            <hr>
            <div class="mensajes">
                <div class="mensaje" v-for="item in mensajes">
                    <MensajeDer :mensaje="item.mensaje" v-if="item.id == 'der'"/>
                    <MensajeIzq :mensaje="item.mensaje" v-if="item.id == 'izq'"/>
                </div>
            </div>
            <hr>
            <div class="enviar-mensaje">
                <input type="text" placeholder="Enviar Mensaje">
                <button @click="enviar()">Enviar</button>
            </div>
        </div>
    </div>
    </template>
<style>
header{
    display: flex;
    flex-direction: row;
}
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
    height: 100vh;
    margin: 0px;
    padding: 10px;
    color:lightcoral;
    background-color: beige;
}
.buscador{
    width: 100%;
}
.buscador span{
    position: relative;
    top: 5px;
    right: 30px;
}

header .iconos .material-icons{
    cursor: pointer;
    transition: all 0.15s ease-in-out;
}

header .iconos .material-icons:hover{
    transform: translateY(-3px);
}
.sidebar{
    background-color: white;
    margin: 0px;
    padding: 10px;
    border-radius: 15px;
}
.chatscontenedor{
    height: 45%;
}
.contactoscontenedor{
    height: 45%;
}

.chats{
    height: 85%;
    overflow-y: scroll;
}
.contactos{
    height: 85%;
    overflow-y: scroll;
}

.chatbox{
    background-color: white;
    margin: 0px;
    margin-left: 10px;
    padding: 10px;
    display: flex;
    flex-direction: column;
    justify-content: end;
    position: relative;
    width: 100%;
}
.mensajes{
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: end;
}

.enviar-mensaje{ 
    margin-top: 10px;
    display: flex;
    flex-direction: row;
    justify-content: end;
}

.enviar-mensaje input{
    margin: 0;
    width: 100%;
}

.chatbox .enviar-mensaje button{
    background-color: lightcoral;
    color: white;
    padding:10px;
    border-radius: 15px;
    padding: 8px;
    margin-left: 10px;
    min-width: 80px;
    transition: all 0.15s ease-in-out;
}
.chatbox .enviar-mensaje button:hover{
    transform: translateY(-3px);
}

</style>

<script setup lang="ts">
  import ContactCard from './ContactCard.vue';
  import ChatCard from './ChatCard.vue'
  import MensajeDer from './MensajeDer.vue';
  import MensajeIzq from './MensajeIzq.vue';

  var mensajes=[
    {id: "izq", mensaje:"Hola"},
    {id: "der", mensaje:":)"},
    {id: "izq", mensaje:"Prueba mensaje"}
]

  function enviar() {
    mensajes.push({id:"izq", mensaje: "hola"})
    console.log(mensajes);
    //en esta funcion se debe actualizar el div.mensajes para ver los mensajes actualizados al enviar uno nuevo
  }

  function buscar() {
    alert("Buscar")
  }
  function llamar() {
    alert("Llamar contacto")
  }
  function videollamar() {
    alert("Videollamar contacto")
  }

</script>