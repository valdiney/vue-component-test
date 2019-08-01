<template>
    <div class="album text-muted">
        <div class="row">
            
            <div class="col-sm-4 card" v-for="usuario in dataUsuarios">
                
                <div class="card-body">
                    <img v-bind:src="usuario.id_face">
                    <h4 class="card-title">{{usuario.nome}}</h4>
                    <p class="card-text">
                        <b>E-mail:</b> {{usuario.email}} <br>
                        <b>Gênero:</b> {{usuario.genero}}
                    </p>
                    <a href="#" class="card-link">Card link</a>
                    <a href="#" class="card-link">Another link</a>
                </div>
                
            </div>

        </div>
    </div>
</template>

<script lang="ts">
import axios from 'axios'
export default {
    name: "Usuarios",
    props: {
        idCliente: ''
    },

    data() {
        return {
            dataUsuarios: 0
        }
    },

    created: function() {
        this.buscarUsuarios(this.idCliente);
        console.log(this.idCliente);
    },

    methods: {
        buscarUsuarios(idCliente) {
            let url = "https://go.wifiaqui.com.br/api/visitantes/"+idCliente;
            
            axios(url).then(response => {
                this.dataUsuarios = response.data;
            })
        }
    }
}
</script>

<style scoped>
.div-interna-card {
    padding:10px!important;
}
.card {
    border-left:0;
    border-bottom:0
}

img {
    width:60px;
    border-radius:50%
}
</style>
                                                                                                                                                                                                          