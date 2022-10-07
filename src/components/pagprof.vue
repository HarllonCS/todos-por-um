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
                                    <button type="button" class="btn mt-3 fw-bold">
                                        <span class="material-icons">logout</span>
                                        <sup>Sair</sup>
                                    </button>
                                </div>
                                <hr>

                                <ul class="list-group list-group-flush ms-2 text-start">
                                    <li class="list-group-item fw-bold mb-2">
                                        <a class="text-decoration-none" href="index.vue">Início</a>
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
                <!--
                <div class="d-grid gap-2 col-6 mx-auto">
                    <button type="button" class="btn text-light fw-bold fs-4">
                        1º ANO A - MANHÃ
                    </button>

                    <button type="button" class="btn text-light fw-bold fs-4">
                        3º ANO B - TARDE
                    </button>

                    <button type="button" class="btn text-light fw-bold fs-4">
                        2º ANO B - TARDE
                    </button>
                </div>-->

                <p class="sala fw-bold text-uppercase">1º ano - A - Manhã</p>

                <div id="acordeao" class="accordion overflow-auto mx-auto border border-2 rounded">
                    <div class="accordion-item" id="accordion-1">
                        <h2 class="accordion-header" id="accordion-header-1">
                            <button class="accordion-button collapsed fw-bold" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-1" aria-expanded="false" aria-controls="accordion-collapse-1">
                                <p class="col">FULANO</p>
                                    
                                <img class="me-3 fs-6" src="./imgs/fita.png" alt="Aluno(a) deficiente" title="Este aluno(a) possui deficiência.">

                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-1" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-1">
                            <div class="accordion-body mx-auto">
                                <div class="d-flex">
                                    <div class="col text-start fw-bold">
                                        <p>Nome:</p>
                                        <p>Sobrenome:</p>
                                        <p>Data de Nascimento:</p>
                                        <p>Sexo:</p>
                                        <p>Tipo Sanguíneo:</p>
                                        <p>Deficiência:</p>
                                        <p>Nome do pai:</p>
                                        <p>Nome da mãe:</p>
                                        <p>E-mail:</p>
                                        <p>Número:</p>
                                        <p>Endereço:</p>
                                    </div>

                                    <div class="col text-end">
                                        <p>Fulano</p>
                                        <p>de Tal</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="accordion-item" id="accordion-2">
                        <h2 class="accordion-header" id="accordion-header-2">
                            <button class="accordion-button collapsed fw-bold d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-2" aria-expanded="false" aria-controls="accordion-collapse-2">
                                <p class="col">CICLANO</p>
                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-2" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-2">
                            <div class="accordion-body mx-auto">
                                <div class="d-flex">
                                    <div class="col text-start fw-bold">
                                        <p>Nome:</p>
                                        <p>Sobrenome:</p>
                                        <p>Data de Nascimento:</p>
                                        <p>Sexo:</p>
                                        <p>Tipo Sanguíneo:</p>
                                        <p>Deficiência:</p>
                                        <p>Nome do pai:</p>
                                        <p>Nome da mãe:</p>
                                        <p>E-mail:</p>
                                        <p>Número:</p>
                                        <p>Endereço:</p>
                                    </div>

                                    <div class="col text-end">
                                        <p>Ciclano</p>
                                        <p>de Tal</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="accordion-item" id="accordion-3">
                        <h2 class="accordion-header" id="accordion-header-3">
                            <button class="accordion-button collapsed fw-bold d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-3" aria-expanded="false" aria-controls="accordion-collapse-3">
                                <p class="col">BEUTRANO</p>
                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-3" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-3">
                            <div class="accordion-body mx-auto">
                                <div class="d-flex">
                                    <div class="col text-start fw-bold">
                                        <p>Nome:</p>
                                        <p>Sobrenome:</p>
                                        <p>Data de Nascimento:</p>
                                        <p>Sexo:</p>
                                        <p>Tipo Sanguíneo:</p>
                                        <p>Deficiência:</p>
                                        <p>Nome do pai:</p>
                                        <p>Nome da mãe:</p>
                                        <p>E-mail:</p>
                                        <p>Número:</p>
                                        <p>Endereço:</p>
                                    </div>

                                    <div class="col text-end">
                                        <p>Beutrano</p>
                                        <p>de Tal</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="accordion-item" id="accordion-4">
                        <h2 class="accordion-header" id="accordion-header-4">
                            <button class="accordion-button collapsed fw-bold d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-4" aria-expanded="false" aria-controls="accordion-collapse-4">
                                <p class="col">REBOCO DE PAREDE</p>

                                <img class="me-3 fs-6" src="./imgs/fita.png" alt="Aluno(a) deficiente" title="Este aluno(a) possui deficiência.">

                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-4" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-4">
                            <div class="accordion-body mx-auto">
                                <div class="d-flex">
                                    <div class="col text-start fw-bold">
                                        <p>Nome:</p>
                                        <p>Sobrenome:</p>
                                        <p>Data de Nascimento:</p>
                                        <p>Sexo:</p>
                                        <p>Tipo Sanguíneo:</p>
                                        <p>Deficiência:</p>
                                        <p>Nome do pai:</p>
                                        <p>Nome da mãe:</p>
                                        <p>E-mail:</p>
                                        <p>Número:</p>
                                        <p>Endereço:</p>
                                    </div>

                                    <div class="col text-end">
                                        <p>Reboco</p>
                                        <p>de Parede</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="accordion-item" id="accordion-5">
                        <h2 class="accordion-header" id="accordion-header-5">
                            <button class="accordion-button collapsed fw-bold
                            d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-5" aria-expanded="false" aria-controls="accordion-collapse-5">
                                <p class="col">ALBEU</p>
                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-5" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-5">
                            <div class="accordion-body mx-auto">
                                <div class="d-flex">
                                    <div class="col text-start fw-bold">
                                        <p>Nome:</p>
                                        <p>Sobrenome:</p>
                                        <p>Data de Nascimento:</p>
                                        <p>Sexo:</p>
                                        <p>Tipo Sanguíneo:</p>
                                        <p>Deficiência:</p>
                                        <p>Nome do pai:</p>
                                        <p>Nome da mãe:</p>
                                        <p>E-mail:</p>
                                        <p>Número:</p>
                                        <p>Endereço:</p>
                                    </div>

                                    <div class="col text-end">
                                        <p>Albeu</p>
                                        <p>da Silva</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="accordion-item" id="accordion-6">
                        <h2 class="accordion-header" id="accordion-header-6">
                            <button class="accordion-button collapsed fw-bold d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-6" aria-expanded="false" aria-controls="accordion-collapse-6">
                                <p class="col">PEDRINHO BIGODE</p>

                                <!--<span class="material-icons fs-1 me-3">all_inclusive</span>-->

                                <img class="me-3 fs-6" src="./imgs/fita.png" alt="Aluno(a) deficiente" title="Este aluno(a) possui deficiência.">

                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-6" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-6">
                            <div class="accordion-body mx-auto">
                                <div class="d-flex">
                                    <div class="col text-start fw-bold">
                                        <p>Nome:</p>
                                        <p>Sobrenome:</p>
                                        <p>Data de Nascimento:</p>
                                        <p>Sexo:</p>
                                        <p>Tipo Sanguíneo:</p>
                                        <p>Deficiência:</p>
                                        <p>Nome do pai:</p>
                                        <p>Nome da mãe:</p>
                                        <p>E-mail:</p>
                                        <p>Número:</p>
                                        <p>Endereço:</p>
                                    </div>

                                    <div class="col text-end">
                                        <p>Pedrinho</p>
                                        <p>Bigode</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="accordion-item" id="accordion-7">
                        <h2 class="accordion-header" id="accordion-header-7">
                            <button class="accordion-button collapsed fw-bold d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-7" aria-expanded="false" aria-controls="accordion-collapse-7">
                                <p class="col">CARA DE PERCATA</p>
                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-7" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-7">
                            <div class="accordion-body mx-auto">
                                <div class="d-flex">
                                    <div class="col text-start fw-bold">
                                        <p>Nome:</p>
                                        <p>Sobrenome:</p>
                                        <p>Data de Nascimento:</p>
                                        <p>Sexo:</p>
                                        <p>Tipo Sanguíneo:</p>
                                        <p>Deficiência:</p>
                                        <p>Nome do pai:</p>
                                        <p>Nome da mãe:</p>
                                        <p>E-mail:</p>
                                        <p>Número:</p>
                                        <p>Endereço:</p>
                                    </div>

                                    <div class="col text-end">
                                        <p>Cara</p>
                                        <p>de Percata</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="accordion-item" id="accordion-8">
                        <h2 class="accordion-header" id="accordion-header-8">
                            <button class="accordion-button collapsed fw-bold d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-8" aria-expanded="false" aria-controls="accordion-collapse-8">
                                <p class="col">ZÉ</p>
                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-8" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-8">
                            <div class="accordion-body mx-auto">
                                <div class="d-flex">
                                    <div class="col text-start fw-bold">
                                        <p>Nome:</p>
                                        <p>Sobrenome:</p>
                                        <p>Data de Nascimento:</p>
                                        <p>Sexo:</p>
                                        <p>Tipo Sanguíneo:</p>
                                        <p>Deficiência:</p>
                                        <p>Nome do pai:</p>
                                        <p>Nome da mãe:</p>
                                        <p>E-mail:</p>
                                        <p>Número:</p>
                                        <p>Endereço:</p>
                                    </div>

                                    <div class="col text-end">
                                        <p>Zé</p>
                                        <p>do Bagaço</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                        <p>X</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </main>
        </div>
    </div>
</template>

<style scoped>

    /*! Generated by Font Squirrel (https://www.fontsquirrel.com) on May 19, 2021 */
    
    /* FONTES QUE ESTÃO SENDO E PODEM SER UTILIZADAS */

    @font-face {
        font-family: 'poppinsblack';
        src: url('fonts/poppins-black-webfont.woff2') format('woff2'),
             url('fonts/poppins-black-webfont.woff') format('woff');
        font-weight: normal;
        font-style: normal;
    }
    
    @font-face {
        font-family: 'poppinsbold';
        src: url('fonts/poppins-bold-webfont.woff2') format('woff2'),
             url('fonts/poppins-bold-webfont.woff') format('woff');
        font-weight: normal;
        font-style: normal;
    }
    
    @font-face {
        font-family: 'poppinslight';
        src: url('fonts/poppins-light-webfont.woff2') format('woff2'),
             url('fonts/poppins-light-webfont.woff') format('woff');
        font-weight: normal;
        font-style: normal;
    }
    
    @font-face {
        font-family: 'poppinsmedium';
        src: url('fonts/poppins-medium-webfont.woff2') format('woff2'),
             url('fonts/poppins-medium-webfont.woff') format('woff');
        font-weight: normal;
        font-style: normal;
    }
    
    @font-face {
        font-family: 'poppinsregular';
        src: url('fonts/poppins-regular-webfont.woff2') format('woff2'),
             url('fonts/poppins-regular-webfont.woff') format('woff');
        font-weight: normal;
        font-style: normal;
    }
    
    @font-face {
        font-family: 'poppinssemibold';
        src: url('fonts/poppins-semibold-webfont.woff2') format('woff2'),
             url('fonts/poppins-semibold-webfont.woff') format('woff');
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

    .navbar-brand span {
        color: #00a7aa;
    }
    
    
    /* Botão de configurações */

    .container-fluid .perfil {
        color: #00a7aa;
        transition: .3s;
        text-decoration: none;
    }

    .container-fluid .perfil:hover {
        color: #019092;
        text-decoration: underline;
        text-decoration-thickness: 1.5px;
    }


    /* Menu de navegação */
    
    .list-group-item {
        border-bottom: 0;
    }

    .list-group-item a {
        transition: .3s;
    }

    .list-group-item a:hover {
        color: #00a7aa;
    }


    /* Botão de sair */

    .offcanvas-body button span {
        font-size: 1.5vw;
    }

    .offcanvas-body button sup {
        font-size: .9vw;
        margin-left: .8vw;
    }

    .offcanvas-body button {
        border-radius: 30px;
        padding-bottom: 0;
    }

    .offcanvas-body button:hover {
        background-color: #00a7aa;
        color: white;
    }


    /* Tela do(a) professor(a) */

    main {
        margin-top: 6vw;
    }

    .sala {
        font-size: 2vw;
    }

    .accordion {
        width: 90%;
        height: 45.3vh;
    }

    .d-grid button {
        background-color: #00a7aa;
        margin-bottom: 1.3vw;
    }

    .d-grid button:hover {
        background-color: #009092;
    }

    .accordion-header button {
        font-size: 1.3vw;
    }

    main .accordion-button {
        background-color: white;
        border: 1px solid #00a7aa;
        color: #00a7aa;
        transition: .3s;
    }

    .accordion-button:hover {
        background-color: #00babd4d;
        color: white;
        border-color: #00babd4d;
    }


    /* Corpo do accordion */

    .accordion-body {
        font-size: .9vw;
        width: 75%;
    }

    .accordion-body p {
        border-bottom: 1px solid #00a7aa;
    }

    
    /* ESTILIZAÇÃO DO MENÚ RESPONSIVO */
    
    @media (max-width: 767.98px) {
    
        .cont {
            width: 95vw;
        }

        /* Título "Todos Por Um" */
    
        .navbar-brand h1 {
            font-size: 5vw;
            line-height: 4.2vw;
        }

        
        /* Botão de "Meu Perfil" */

        .container-fluid .perfil {
            font-size: 5vw;
        }


        /* Botão de sair */

        .offcanvas-body button span {
            font-size: 7vw;
        }

        .offcanvas-body button sup {
            font-size: 4vw;
            margin-left: 3vw;
        }


        /* Título da sala */

        .sala {
            font-size: 6vw;
        }


        /* Accordion */

        .accordion {
            width: 90%;
            height: 49.8vh;
        }

        .accordion-header button {
            font-size: 5vw;
        }

        .accordion img {
            width: 10vw;
        }

        .accordion-body {
            font-size: 3.2vw;
            width: 100%;
        }

    }

    @media (min-width: 768px) and (max-width: 1199.98px) {
         
        /* Botão de "Meu Perfil" */

        .container-fluid .perfil {
            font-size: 3vw;
        }

        /* Título da sala */

        .sala {
            font-size: 4vw;
        }
        
        /* Accordion */

        .accordion {
            width: 90%;
            height: 44.4vh;
        }

        .accordion-header button {
            font-size: 2.5vw;
        }

        .accordion-body {
            font-size: 2vw;
            width: 85%;
        }

        /* Botão de sair */

        .offcanvas-body button span {
            font-size: 3.5vw;
        }

        .offcanvas-body button sup {
            font-size: 2.2vw;
            margin-left: 3vw;
        }

        .list-group {
            font-size: 2.5vw;
        }
    }

    @media (min-width: 1200px) and (max-width: 1399.98px) {
        /* Botão de "Meu Perfil" */

        .container-fluid .perfil {
            font-size: 1.6vw;
        }

        /* Botão de sair */

        .offcanvas-body button span {
            font-size: 2vw;
        }

        .offcanvas-body button sup {
            font-size: 1.2vw;
            margin-left: 1.5vw;
        }

        .list-group {
            font-size: 1.8vw;
        }
    }
</style>