<template>
  <section id="app">

        <header class="header">
            <img class="logoVue" src="./assets/logo.png">
            <h4 class="logo">{{titulo}}</h4>
        </header>   
        <main class="main">
            <h1 class="tituloMain">Componente Tabla</h1>
            <p class="textoMain">Renderizar varias veces un componente Table con algunas cosas customizables y tomando datos de diferentes fuentes</p>
            <article class="contenedorTabla" >
                <MiTabla :tabledata="grupoa" titulo="Grupo A" tablestyle="table-info" backgroundheader="text-bg-info"></MiTabla>
                <MiTabla :tabledata="grupob" titulo="Grupo B" tablestyle="table-warning" backgroundheader="text-bg-warning"></MiTabla>
                <MiTabla :tabledata="grupoc" titulo="Grupo C" tablestyle="table-success" backgroundheader="text-bg-success"></MiTabla>
            </article>
        </main>
        <footer class="footer">
            <h6>Hola soy el Footer</h6>
        </footer>
    </section>
</template>

<script>
import MiTabla from './components/MiTabla.vue'

export default {
  name: 'App',
  components: {
    MiTabla
  },
  data(){
    return{
        titulo:"Guille Chiantore - Desafio Creacion de componentes en Vue - Tablas",
        columnas:{
            col1:"ISO",
            col2:"Pais",
            col4:"imagen"
        },
        grupoa:[
            {
                iso:"AR",
                pais:"Argentina",
                imagen:"ar.png"
            },
            {
                iso:"BR",
                pais:"Brasil",
                imagen:"br.png"
            },
            {
                iso:"NL",
                pais:"Netherland",
                imagen:"nl.png"
            },
            {
                iso:"ES",
                pais:"España",
                imagen:"es.png"
            },
        ],
        grupob:[
            {
                iso:"US",
                pais:"Australia",
                imagen:"au.png"
            },
            {
                iso:"GH",
                pais:"Ghana",
                imagen:"gh.png"
            },
            {
                iso:"FR",
                pais:"Francia",
                imagen:"fr.png"
            },
            {
                iso:"CA",
                pais:"Canada",
                imagen:"ca.png"
            }
        ],
        grupoc:[
            {
                iso:"US",
                pais:"Estados Unidos",
                imagen:"us.png"
            },
            {
                iso:"CR",
                pais:"Costa Rica",
                imagen:"cr.png"
            },
            {
                iso:"IR",
                pais:"Iran",
                imagen:"ir.png"
            },
            {
                iso:"SA",
                pais:"Arabia Saudita",
                imagen:"sa.png"
            },
        ],  
      }
    }  
  }

</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Ubuntu:ital,wght@0,300;0,400;0,500;0,700;1,300;1,400;1,500;1,700&display=swap');
*{
    margin:0px;
    padding:0px;
    font-family: 'Ubuntu', sans-serif;
}

.header{
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color:#19234F;
    color:#BDAA75;
}

.logo{
    
    font-weight: 100;
    margin: 10px;
}

.main{
    width: 100%;
    padding-top:100px;
    padding-bottom: 100px;
    display: flex;
    align-items: center;
    flex-direction: column;
    background-color:lightgrey;
    color:#000000;
}
.tituloMain{
    margin: 15px;
}

.textoMain{
    margin: 10px;
    font-weight: 100;
    text-align: center;
}

.contenedorTabla{
    width: 100%;
    display: flex;
    align-items: center;
    justify-content:center;
    flex-direction: row;
    flex-wrap:wrap;
    row-gap: 10px;
    column-gap: 10px;
    color:#BDAA75;
}

.tituloMain{
    margin: 15px;
}

.logoVue{
  width: 50px;
  height: 50px;
}
.textoMain{
    margin: 10px;
    font-weight: 100;
    text-align: center;
}

.contenedorTabla{
    width: 100%;
    display: flex;
    align-items: center;
    justify-content:center;
    flex-direction: row;
    flex-wrap:wrap;
    row-gap: 10px;
    column-gap: 10px;
    color:#BDAA75;
}

.footer{
    width: 100%;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color:#19234F;
    color:#BDAA75;
}
</style>
