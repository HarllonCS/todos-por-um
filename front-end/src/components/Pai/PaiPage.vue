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
                            <div class="offcanvas-body">
                                <img src="https://picsum.photos/180" class="d-block mx-auto rounded-circle">

                                <h5 class="fw-bold text-uppercase text-center mt-3">nome</h5>

                                <div class="text-start">
                                    <button type="button" class="btn mt-3 fw-bold" v-on:click="logout">
                                        <span class="material-icons">logout</span>
                                        <sup>Sair</sup>
                                    </button>
                                </div>
                                <hr>

                                <ul class="list-group list-group-flush ms-2 text-start">
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
    
            <!-- Botão para cadastrar aluno -->
            <button type="button" class="table-btn float-right p-2 rounded border-0" data-bs-toggle="modal" data-bs-target="#alunoCadastro" title="Cadastrar novo(a) aluno(a)">
                    <span class="material-icons text-light">add</span>
            </button> <!-- /fim do Botão para cadastrar aluno -->
         
            <!-- Modal -->
            <CadastroPai/>

            <main role="main" id="abc">
                <!-- Tabela de alunos acadastrados (pais ou responsáveis) -->
                <table class="table table-striped table-bordered mx-auto text-center shadow">
                    <!-- Cabeçalho da tabela -->
                    <thead class="text-light">
                        <th scope="col">ID</th>
                        <th scope="col">NOME</th>
                        <th scope="col">ANO E TURMA</th>
                        <th scope="col">TURNO</th>
                        <th scope="col"></th>
                    </thead> <!-- /fim do Cabeçalho da tabela -->

                    <tbody> <!-- Corpo da tabela -->
                        <tr v-for="retornoBd in retornoBd" :key="retornoBd.id">
                            <th scope="row">{{retornoBd.id}}</th>
                            <td>{{retornoBd.nome}}</td>
                            <td>{{retornoBd.turma}}</td>
                            <td>{{retornoBd.turno}}</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Deletar" @click="removeAlunoBd(retornoBd.id)">delete</span>
                                    <span class="material-icons" title="Editar">edit</span>
                                </div>
                            </td>
                        </tr>
                    </tbody> <!-- /fim Corpo da tabela -->
                </table>  <!-- /fim Tabela -->
            </main>
        </div>
    </div>
</template>

<script>
import Axios from "@/services/restApi/restServices"
import CadastroPai from "./cadastro-modal/CadastroPai.vue";


    export default {
    name: "PaiPage",
    data() {
        return {
            retornoBd: null,
            tokenPai: {
              token: this.$store.state.token
            }
        };
    },
    methods: {
        async getAlunosBd() {
            //chamando os dados do back
            Axios.getPai(this.tokenPai).then(resposta => {this.retornoBd = resposta.data})
            console.log(this.retornoBd)
        
        },
        async logout() {
            this.$store.commit("logout");
        }
    },
    mounted() {
        this.getAlunosBd();
        console.log(this.tokenPai)
    },
    components: { CadastroPai }
}
</script>

<style scoped>
    /*! Generated by Font Squirrel (https://www.fontsquirrel.com) on May 19, 2021 */
    
    /* FONTES QUE ESTÃO SENDO UTILIZADAS */
    
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
    
    
    /* Formatação do Cabeçalho (logo) */
    
    .navbar-brand h1 {
        font-size: 3vw;
        line-height: 2.8vw;
    }
    
    .navbar-brand a {
        text-decoration: none;
    }
    

    /* Tabela */
    
    table {
        font-size: 1vw;
        width: 45vw;
    }

    .table-btn {
        margin-left: 60vw;
        cursor: pointer;
        background-color: hsl(181, 100%, 33%);
        transition: .3s;
    }
    
    .table-btn:hover {
        background-color: #019092;
    }
    
    thead {
        background-color: #00a7aa;
    }
    
    
    /* ESTILIZAÇÃO DO MENÚ RESPONSIVO */
    
    
    @media (min-width: 320px) and (max-width: 767.98px) {
        .cont {
            width: 100%;
            padding: 1vw;
        }

        /* Título "Todos Por Um" */
    
        .navbar-brand h1 {
            font-size: 5vw;
            line-height: 4.2vw;
        }

        .offcanvas-body button {
            background-color: #00a7aa;
            color: white;
        }
    
        .table-btn {
            display: block;
            font-size: 0;
            margin: auto;
        }

        table {
            width: 100%;
        }

        thead {
            font-size: 3.2vw;
        }
    }

    @media (min-width: 768px) and (max-width: 991.98px) {
        a.perfil {
            font-size: 90%;
        }

        .table-btn {
            display: block;
            font-size: 0;
            margin: auto;
        }

        table {
            width: 85%;
        }

        thead {
            font-size: 1.8vw;
        }
    }

    @media (min-width: 992px) and (max-width: 1399.98px) {
        a.perfil {
            font-size: 90%;
        }

        table {
            width: 90%;
        }

        thead {
            font-size: 1.5vw;
        }

        .offcanvas-body span {
            font-size: 2.8vw;
        }

        .offcanvas-body sup {
            font-size: 1.7vw;
            margin-left: 1.8vw;
        }
    }
</style>