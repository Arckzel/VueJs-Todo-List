<template>
    <div class="Cabecalho">
        <div class="icone">
            <a href=""><h1>{{ nome }}</h1></a>
        </div>
        <div class="botoes">
            <ul>
                <li><a href="" target="_blank" rel="noopener">Nova Aba</a></li>
                <li><a href="" >Botão 2</a></li>
                <li><a href="" >Botão 3</a></li>
                <li><a href="" >Botão 4</a></li>
            </ul>
        </div>
        <!-- <div class="buscador">
            <div class="inputebutton">
                <form action="" method="get">
                    <input type="text" name="busca" id="busca">
                    <button type="submit">Buscar</button>
                </form>        
            </div>
            
        </div>       -->
    </div>
</template>

<script>
export default {
    name: 'Cabecalho',
    props: {
        nome: String
    }
}
</script>

<style scoped>
h1{
        color: black;
    /* margin: 10% 0px 0px 0px; */
    box-shadow: 0px 0px 5px -3px black;
    border-radius: 10px;
    padding: 0px 20px;
    width: -webkit-fit-content;
    width: -moz-fit-content;
    width: fit-content;
    margin: 20px auto !important;
    text-shadow: -5px 7px 4px darkgrey;
}
ul{
    margin: 4% 0px 0px 0px;
    padding: 0;
}
li{
    display: inline-block;
    margin: 0px 10px;   
}
li a{
    background-color: white;
    padding: 5px 14px;
    box-shadow: 0px 0px 5px -3px black;
    border-radius: 5px;
    color: black;
    text-decoration: none;
}
li a:hover{    
    font-size: 10;
    box-shadow: inset 0px 0px 4px -2px black;
}
a{
    text-decoration: none;
}
.Cabecalho{
    background-color: white;
    display: flex;
}

.icone{
    min-width: 25%;
}
.botoes{
    min-width: 50%;
    padding: 0;
    margin: 0% 0px 0px 0px;    
}

.buscador{
    min-width: 25%;
}
.inputebutton{
    margin: 8% 0px 0px 0px;
}
input{
    margin: 0;
}
button{
    margin: 0px 0px 0px 10px;
}

</style>