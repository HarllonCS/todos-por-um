<template>
    <div class="body">
        <div class="cont mx-auto"> 
            <header><!-- início Cabeçalho -->
                <nav class="navbar navbar-expand-lg"><!-- Menu -->
                    <div class="container-fluid">
                        <div class="navbar-brand text-start"><!-- Logotipo "Todos Por Um" -->
                            <a href="index.html">
                                <h1 class="fw-bold text-dark"><span>TODOS</span><br>POR UM</h1>
                            </a>
                        </div><!-- /fim Logotipo "Todos Por Um" -->
                        
                        <!-- Menu responsivo -->
                        <!-- Botão "hambúrguer" do menu responsivo -->
                        <button class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#navegacao" aria-controls="navbarToggleExternalContent" aria-expanded="false" aria-label="Toggle navigation">
                            <span class="navbar-toggler-icon"></span>
                        </button>
                        <!-- /fim Botão "hambúrguer" do menu responsivo -->

                        <div id="navegacao" class="collapse navbar-collapse">
                            <ul class="navbar-nav ms-auto">
                                <li class="nav-item fw-bold">
                                    <a href="index.html" class="nav-link ativo">Início</a>
                                </li>

                                <li class="nav-item fw-bold">
                                    <a href="#" class="nav-link">Serviços</a>
                                </li>

                                <li class="nav-item fw-bold">
                                    <a href="#" class="nav-link">Sobre</a>
                                </li>

                                <li class="nav-item fw-bold">
                                    <a href="#" class="nav-link">Contato</a>
                                </li>
                            </ul>
                        </div>
                    </div><!-- /fim Menu responsivo -->
                </nav> <!-- /fim Menu -->
            </header> <!-- /fim Cabeçalho -->
            
            <main role="main" class="d-flex justify-content-between mt-2"> <!-- Tela de login -->
                <aside class="shadow"> <!-- Texto e formulário -->
                    <!-- Texto da tela de login -->
                    <h2 class="fw-bold">
                        <span>Comece agora!</span><br>Junte-se a nós.
                    </h2><!-- /fim Texto da tela de login -->
                        
                    <form @submit="tryLogin"><!-- Formulário da tela de login -->

                        <div class="login-inputs d-flex flex-column">
                            <input type="email" class="form-control" name="email" placeholder="E-mail" v-model="userLogin.email" required autofocus>

                            <input type="password" class="form-control mt-4" placeholder="Senha" name="senha" v-model="userLogin.senha" required>
                        </div>

                        <div class="login-btn d-flex justify-content-between mt-4">
                            <input type="submit" class="btn fw-bold text-light" value="ENTRAR">

                            <a class="fw-bold" type="button" data-bs-toggle="modal" data-bs-target="#modalPais">Cadastrar</a>
                        </div>
                    </form> <!-- /fim Formulário da tela de login -->
                </aside> <!-- /fim Texto e formulário -->
    
                <!-- Modal de escolha -->
                <!-- <div class="modal fade" id="modalEscolha" aria-hidden="true" aria-labelledby="labelEstatico" tabindex="-1" data-bs-backdrop="static" data-bs-keyboard="false">
                    <div class="modal-dialog modal-dialog-centered">
                        <div class="modal-content">
                            <div class="modal-header">
                                <h5 class="modal-title fw-bold" id="labelEstatico">Professor(a) ou responsável?</h5>

                                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                            </div>

                            <div class="modal-body">
                                <div class="d-flex justify-content-around">
                                    <button class="btn btn-primary fw-bold p-2">SOU PROFESSOR(A)</button>
                                    <button class="btn btn-success fw-bold p-2" data-bs-target="#modalPais" data-bs-toggle="modal">SOU RESPONSÁVEL</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div> -->

                <Cadastro/> <!-- Chamando a modal do cadastro -->

                <article> <!-- Imagem de crianças pulando -->
                    <img src="@/assets/imgs/login-gif.svg" alt="Crianças pulando alegremente">
                </article> <!-- /fim Imagem de crianças pulando -->
            </main> <!-- /fim Tela de login -->
        </div>
    </div>
</template>

<script>
import router from '@/router';
import Axios from "@/services/restApi/restServices";
import Cadastro from './cadastro-modal/Cadastro.vue';
import Functions from "@/services/functions"

export default {
    name: "LoginPage",
    data() {
        return {
            userLogin: {
                email: "",
                senha: ""
            },
            dadosBack: null,
            encaminhamento: {
                token: "",
                acesso: "",
                nome: ""
            }
        };
    },
    methods: {
        async tryLogin(e) {
            e.preventDefault();
            
            
           Functions.tryLogin1(this.userLogin); 
            //metodo Post com os dados do userLogin
           Axios.save(this.userLogin).then(resposta => {
                this.dadosBack = resposta.data; //recebendo os valores que o post gerou
                for (let elemento of this.dadosBack) {
                    this.encaminhamento.acesso = elemento.acesso;
                }
                for (let elemento of this.dadosBack) {
                    this.encaminhamento.token = elemento.token;
                }
                for (let elemento of this.dadosBack) {
                    this.encaminhamento.nome = elemento.nome
                }

                //jogando os dados para o store
                this.$store.commit("saveToken", this.encaminhamento.token);
                this.$store.commit("saveAcesso", this.encaminhamento.acesso);
                this.$store.commit("saveNome", this.encaminhamento.nome);
                this.redirecionamento();
            });
        },

        async redirecionamento() {
            //router.push para redirecionar
            switch (this.$store.state.acesso) {

                case "A": router.push("/pai"); 
                break;
                
                case "P": router.push("/prof");
                break;
                
                //case "": alert("Usuario ou Senha Incorreta!")
                //break;

                //default: alert("Senha incorreta")
                //break;
            }

            if(!this.$store.state.logado) {
                
            } else {
                switch (this.$store.state.acesso) {
                    case "A": router.push("/pai"); 
                    break;
                        case "P": router.push("/prof");
                        break;
                    default: 
                }
            }
        }
    },

    mounted() {
        //RESOLVER ERRO AO CARREGAR A PAGINA
        this.redirecionamento();
        
    },

    components: { Cadastro }
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
    
    /* Menu de navegação */
    .nav-item {
        margin-left: 3.5vw;
        cursor: pointer;
        font-size: .9vw;
    }
    
    .nav-link {
        color: black;
        transition: .3s;
    }
    
    .nav-link:hover, .ativo {
        color: #00a7aa;
    }
    
    .ativo {
        cursor: auto;
    }

    /* Botão do menu responsivo */
    .navbar-toggler {
        background-color: #00a7aa;
    }
    
    /* Textos e inputs */
    aside {
        width: 30vw;
        padding: 2vw;
        border-radius: 10px;
    }
    
    aside h2 {
        font-size: 3.2vw;
        line-height: 3vw;
        font-family: 'poppinsmedium';
    }
    
    aside span, .navbar-brand span {
        color: #00a7aa;
    }
    
    /* Formatação dos campos (inputs) */
    aside [type="email"], aside [type="password"] {
        margin-top: 1.2vw;
        font-size: .9vw;
        padding: 1vw;
        border-radius: 10px;
    }
    
    /* Botões */
    .login-btn input {
        padding: .7vw 1.8vw;
        background-color: #00a7aa;
        border-radius: 30px;
        transition: .3s;
        font-size: .95vw;
    }
    
    .login-btn input:hover {
        background-color: #00c0c4;
    }
    
    .login-btn a {
        color: #00a7aa;
        margin-top: .8vw;
        text-decoration: none;
        font-size: .9vw;
    }
    
    .login-btn a:hover {
        text-decoration: underline;
        color: #008183;
        text-decoration-thickness: 1.5px;
    }
    
    /* Imagem animada */
    img {
        width: 28vw;
    }
    
    /* ESTILIZAÇÃO RESPONSIVA */
    @media (max-width: 767.98px) {

        .cont {
            width: 95%;
        }

        /* Título "Todos Por Um" */
        .navbar-brand h1 {
            font-size: 5vw;
            line-height: 4.2vw;
        }
    
        /* Opções do menú: "Início", "Serviços", etc... */
        nav ul {
            margin-top: 5vw;
        }

        .nav-item {
            margin-bottom: 5vw;
        }
    
        .nav-link {
            font-size: 5vw;
        }
    
        aside {
            width: 100%;
        }
    
        aside h2 {
            font-size: 8vw;
            text-align: center;
            line-height: 9vw;
        }
    
        aside input[type="email"], aside input[type="password"] {
            font-size: 5vw;
            padding: 3vw;
            margin-top: 1vw;
        }
    
        /* Botões */
        .login-btn {
            flex-direction: column;
        }
        
        /* Botão de "ENTRAR" */
        .login-btn input {
            padding: 1.5vw 1vw;
            font-size: 5vw;
            margin-top: 4vw;
        }
    
        /* Link para Cadastrar */
        .login-btn a {
            margin: 6vw auto 0 auto;
            font-size: 4vw;
        }
    
        /* Imagem animada não aparece */
        img {
            display: none;
        }
    }

    @media (min-width: 768px) and (max-width: 1199.98px) {

        /* Opções do menu */
        .nav-item {
            font-size: 1.2vw;
            margin-left: 2.3vw;
        }

        aside {
            width: 32.5vw;
        }

        aside h2 {
            font-size: 3.5vw;
            line-height: 3.5vw;
        }

        img {
            width: 29vw;
        }

        aside [type="email"], aside [type="password"] {
            font-size: 1.3vw;
        }

        .login-btn input {
            font-size: 1.12vw;
        }

        .login-btn a {
            font-size: 1vw;
        }
    }
</style>