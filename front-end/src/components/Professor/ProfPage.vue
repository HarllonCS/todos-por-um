<template>

    <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">

    <div class="body">
        <div class="cont mx-auto">
            <header><!-- início Cabeçalho -->
                <nav class="navbar"><!-- Menu -->
                    <div class="container-fluid">
                        <div class="navbar-brand text-start"><!-- Logotipo "Todos Por Um" -->
                            <a class="text-decoration-none text-dark" href="index.html">
                                <h1 class="fw-bold"><span>TODOS</span><br>POR UM</h1>
                            </a>
                        </div><!-- /fim Logotipo "Todos Por Um" -->
                    
                        <!-- Menu responsivo -->

                        <!-- Botão do menu do usuário -->
                        <a class="perfil" type="button" data-bs-toggle="offcanvas" data-bs-target="#abaLateral" aria-controls="abaLateral">Meu Perfil</a>
                        <!-- /fim Botão do menu do usuário -->

                        <!-- Aba lateral do usuário -->
                        <div class="offcanvas offcanvas-end" tabindex="-1" id="abaLateral" aria-labelledby="abaLateralLabel">
                            <!-- Cabeçalho da aba lateral -->
                            <div class="offcanvas-header">
                                <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
                            </div> <!-- /fim Cabeçalho da aba lateral -->

                            <!-- Corpo da aba lateral -->
                            <div class="offcanvas-body" >
                                <img src="https://picsum.photos/180" class="d-block mx-auto rounded-circle">

                                <h5 class="fw-bold text-uppercase text-center mt-3">{{$store.state.nome}}</h5>

                                <div class="text-start">
                                    <button type="button" class="btn mt-3 fw-bold" v-on:click="logout">
                                        <span class="material-icons">logout</span>
                                        <sup>Sair</sup>
                                    </button>
                                </div>
                                <hr>

                                <ul class="list-group list-group-flush">
                                    <li class="list-group-item fw-bold mb-2">
                                        <a class="text-decoration-none" href="#">Início</a>
                                    </li>

                                    <li class="list-group-item fw-bold mb-2">
                                        <a class="text-decoration-none" href="#">Serviços</a>
                                    </li>

                                    <li class="list-group-item fw-bold mb-2">
                                        <a class="text-decoration-none" href="#">Sobre</a>
                                    </li>
                                    
                                    <li class="list-group-item fw-bold mb-2">
                                        <a class="text-decoration-none" href="#">Contato</a>
                                    </li>
                                </ul>
                            </div> <!-- /fim Corpo da aba lateral -->
                        </div> <!-- /fim Aba lateral do usuário -->
                    </div>
                </nav> <!-- /fim Menu -->
            </header> <!-- /fim Cabeçalho -->

            
            <main role="main">
            <div v-if="!ok">
               <div class="d-grid gap-2 col-6 mx-auto" v-for="retornoBd in retornoBd" :key="retornoBd.id">
                    <button type="button" class="btn text-light fw-bold" v-on:click="getTokenAluno(retornoBd.tokenaluno, retornoBd.sala)">
                        {{retornoBd.sala}}</button>
                </div>
            </div>

            <div v-else>
               <Alunos :SalaTokenalunoPros = "SalaTokenaluno" />  <!-- enviando via props -->
            </div>
            </main>
        </div>
    </div>
</template>

<script>
import Salas from './salas/Salas.vue';
import Alunos from './alunos/Alunos.vue';
import Axios from "@/services/restApi/restServices"



    export default {
    name: "ProfView",
    data() {
        return {
          ok: false,  
          token: {  //token que vai para o servidor
            tokenprof: this.$store.state.token
        }, 
          retornoBd: null,
          SalaTokenaluno: { //objeto que vai enviar via props o token do aluno e nome da sala - parte2
            t: "", //token que vai ser usado para buscar os alunos no banco
            s:"" //string que vai definir o nome da sala no topo da lista de alunos
          },
        }
    },
    components: { Salas, Alunos},
        methods: {
            async logout() {
            this.$store.commit("logout")
        },

        getSalas() { //chamando o banco com o token do professor como parametro
            console.log(this.token)
            Axios.getSala(this.token).then(resposta => { //exibindo as salas do bd
                 this.retornoBd = resposta.data
            })

        },

        getTokenAluno(tokenaluno, sala) { //pegando o token ao clicar no botão
            this.ok = true;

            //enviando o token via props para buscar os alunos no banco - parte1
            this.SalaTokenaluno.t = tokenaluno;
            //enviando nome da sala via props
            this.SalaTokenaluno.s = sala
        
        }

        },
        mounted() {
           
            this.getSalas();

        }

    }

</script>

<style>
    @font-face {
        font-family: 'poppinsmedium';
        src: url('@/assets/fonts/poppins-medium-webfont.woff2') format('woff2'),
             url('@/assets/fonts/poppins-medium-webfont.woff') format('woff');
        font-weight: normal;
        font-style: normal;
    }
    
    @font-face {
        font-family: 'poppinsregular';
        src: url('@/assets/fonts/poppins-regular-webfont.woff2') format('woff2'),
             url('@/assets/fonts/poppins-regular-webfont.woff') format('woff');
        font-weight: normal;
        font-style: normal;
    }

    .body {
        background-color: whitesmoke;
        font-family: 'poppinsregular';
        height: 100vh;
    }
    
    .cont {
        width: 70vw;
        padding: 1vw;
    }

    main {
        margin-top: 2vw;
    }

    /* Formatação do Cabeçalho (logo) */
    .navbar-brand h1 {
        font-size: 3vw;
        line-height: 2.8vw;
    }
    
    /* Botão de configurações */
    .perfil {
        color: #00a7aa;
        transition: .3s;
        text-decoration: none;
    }

    .perfil:hover {
        color: #019092;
        text-decoration: underline;
    }

    /* Botões das salas */
    .d-grid button {
        font-size: 1.3vw;
    }

    /* Botão de logout */
    .offcanvas-body button {
        border-radius: 30px;
        padding-bottom: 0;
    }

    .offcanvas-body button:hover {
        background-color: #00a7aa;
        color: white;
    }

    .offcanvas-body span {
        font-size: 1.5vw;
    }

    .offcanvas-body sup {
        font-size: .9vw;
        margin-left: .8vw;
    }

    /* Menu de navegação */
    li.list-group-item {
        border-bottom: none;
    }

    li.list-group-item a {
        transition: .3s;
        color: black;
    }

    li.list-group-item a:hover {
        color: #00a7aa;
    }

    /* ESTILIZAÇÃO DO MENÚ RESPONSIVO */
    @media (min-width: 320px) and (max-width: 575.98px) {
    
        .cont {
            width: 100%;
        }

        /* Título "Todos Por Um" */
        .navbar-brand h1 {
            font-size: 5vw;
            line-height: 5vw;
        }

        /* Botões das salas */
        .d-grid button {
            font-size: 4vw;
            margin-bottom: 4vw;
        }
    
        /* Botão de logout */
        .offcanvas-body button {
            background-color: #00a7aa;
            color: white;
        }

        .offcanvas-body span {
            font-size: 5vw;
        }

        .offcanvas-body sup {
            font-size: 3.2vw;
            margin-left: 3vw;
        }
    }

    @media (min-width: 576px) and (max-width: 767.98px) {
         
        /* Botão de "Meu Perfil" */
        .perfil {
            font-size: 2.5vw;
        }

        .cont {
            width: 90%;
        }

        /* Botões das salas */
        .d-grid button {
            font-size: 3vw;
        }

        /* Botão de sair */
        .offcanvas-body button {
            background-color: #00a7aa;
            color: white;
        }

        .offcanvas-body span {
            font-size: 3.5vw;
        }

        .offcanvas-body sup {
            font-size: 2.2vw;
            margin-left: 3vw;
        }

        .list-group {
            font-size: 2.5vw;
        }
    }

    @media (min-width: 768px) and (max-width: 1399.98px) {
        
        /* Botão de "Meu Perfil" */
        .perfil {
            font-size: 1.8vw;
        }

        /* Botões das salas */
        .d-grid button {
            font-size: 2.5vw;
        }

        /* Botão de sair */
        .offcanvas-body span {
            font-size: 2.5vw;
        }

        .offcanvas-body sup {
            font-size: 1.6vw;
            margin-left: 1.5vw;
        }

        .list-group {
            font-size: 1.8vw;
        }
    }
</style>