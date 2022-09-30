<template>

    <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">

    <div class="body">
        <div class="cont mx-auto">
            <header class="mb-4"><!-- início Cabeçalho -->
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
                                    <a href="index.html" class="nav-link">Início</a>
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

            <p class="float-end fs-3">Prof. Nome</p>

            <main role="main" class="main-prof">
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

                <p class="fs-1 fw-bold text-uppercase">1º ano - A</p>

                <div id="acordeao" class="accordion overflow-auto w-50 mx-auto border border-2 rounded" style="height: 22.6vw;">
                    <div class="accordion-item" id="accordion-1">
                        <h2 class="accordion-header" id="accordion-header-1">
                            <button class="accordion-button collapsed fw-bold fs-4 d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-1" aria-expanded="false" aria-controls="accordion-collapse-1">
                                <p class="col">FULANO</p>
                                    
                                <span class="material-icons fs-1 me-3">all_inclusive</span>

                                <img src="https://picsum.photos/45" class="border  border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-1" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-1">
                            <div class="accordion-body">
                                    <p>
                                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                    </p>

                                    <p>
                                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                    </p>
                            </div>
                        </div>
                    </div>

                    <div class="accordion-item" id="accordion-1">
                        <h2 class="accordion-header" id="accordion-header-2">
                            <button class="accordion-button collapsed fw-bold fs-4 d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-2" aria-expanded="false" aria-controls="accordion-collapse-2">
                                <p class="col">CICLANO</p>
                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-2" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-2">
                            <div class="accordion-body">
                                    <p>
                                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                    </p>

                                    <p>
                                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                    </p>
                            </div>
                        </div>
                    </div>

                    <div class="accordion-item" id="accordion-3">
                        <h2 class="accordion-header" id="accordion-header-3">
                            <button class="accordion-button collapsed fw-bold fs-4 d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-3" aria-expanded="false" aria-controls="accordion-collapse-3">
                                <p class="col">BEUTRANO</p>
                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-3" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-3">
                            <div class="accordion-body">
                                    <p>
                                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                    </p>

                                    <p>
                                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                    </p>
                            </div>
                        </div>
                    </div>

                    <div class="accordion-item" id="accordion-4">
                        <h2 class="accordion-header" id="accordion-header-4">
                            <button class="accordion-button collapsed fw-bold fs-4 d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-4" aria-expanded="false" aria-controls="accordion-collapse-4">
                                <p class="col">REBOCO DE PAREDE</p>

                                <span class="material-icons fs-1 me-3">all_inclusive</span>

                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-4" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-4">
                            <div class="accordion-body">
                                    <p>
                                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                    </p>

                                    <p>
                                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                    </p>
                            </div>
                        </div>
                    </div>

                    <div class="accordion-item" id="accordion-5">
                        <h2 class="accordion-header" id="accordion-header-5">
                            <button class="accordion-button collapsed fw-bold fs-4 d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-5" aria-expanded="false" aria-controls="accordion-collapse-5">
                                <p class="col">DEBILOIDE</p>
                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-5" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-5">
                            <div class="accordion-body">
                                    <p>
                                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                    </p>

                                    <p>
                                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                    </p>
                            </div>
                        </div>
                    </div>

                    <div class="accordion-item" id="accordion-6">
                        <h2 class="accordion-header" id="accordion-header-6">
                            <button class="accordion-button collapsed fw-bold fs-4 d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-6" aria-expanded="false" aria-controls="accordion-collapse-6">
                                <p class="col">PEDRINHO BIGODE</p>

                                <span class="material-icons fs-1 me-3">all_inclusive</span>

                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-6" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-6">
                            <div class="accordion-body">
                                    <p>
                                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                    </p>

                                    <p>
                                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                    </p>
                            </div>
                        </div>
                    </div>

                    <div class="accordion-item" id="accordion-8">
                        <h2 class="accordion-header" id="accordion-header-8">
                            <button class="accordion-button collapsed fw-bold fs-4 d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-8" aria-expanded="false" aria-controls="accordion-collapse-8">
                                <p class="col">CARA DE PERCATA</p>
                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-8" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-8">
                            <div class="accordion-body">
                                    <p>
                                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                    </p>

                                    <p>
                                        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                    </p>
                            </div>
                        </div>
                    </div>

                    <div class="accordion-item" id="accordion-9">
                        <h2 class="accordion-header" id="accordion-header-9">
                            <button class="accordion-button collapsed fw-bold fs-4 d-flex" type="button" data-bs-toggle="collapse" data-bs-target="#accordion-collapse-9" aria-expanded="false" aria-controls="accordion-collapse-9">
                                <p class="col">JOÃO CACHAÇA</p>
                                <img src="https://picsum.photos/45" class="border border-info rounded-circle me-2">
                            </button>
                        </h2>

                        <div id="accordion-collapse-9" class="accordion-collapse collapse" data-bs-parent="#acordeao" aria-labelledby="accordion-header-9">
                            <div class="accordion-body">
                                <p>
                                    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                </p>

                                <p>
                                    Lorem ipsum, dolor sit amet consectetur adipisicing elit. Dicta nihil nemo neque tempore. Numquam nulla culpa voluptates perspiciatis ratione doloribus dolorum in fuga, illum, laudantium labore quos natus aut! Magnam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Expedita hic magni quisquam et pariatur culpa ratione neque, quae dicta illo vitae beatae eos a fugit praesentium minus inventore sapiente est. Lorem ipsum dolor sit amet consectetur, adipisicing elit. Incidunt cupiditate natus quidem sint rerum eligendi doloremque necessitatibus sunt excepturi. A, repellendus eligendi? Quae at quos alias repellendus illum omnis ut.
                                </p>
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
    
    /* Formatação da tela de login */
    
    main {
        justify-content: space-between;
        margin-top: 2vw;
    }
    
    /* Textos e inputs */
    
    aside {
        width: 30vw;
        padding: 2vw;
        border-radius: 10px;
    }
    
    aside h2 {
        font-size: 3.2vw;
        line-height: 3.3vw;
        font-family: 'poppinsmedium';
    }
    
    aside span, .navbar-brand span {
        color: #00a7aa;
    }
    
    /*
    aside p {
        line-height: 1.3vw;
        font-family: 'poppinslight';
        font-size: .9vw;
    }
    */
    
    /* Formatação dos campos (inputs) */
    
    .login-inputs {
        flex-direction: column;
        font-size: .9vw;
    }
    
    aside [type="email"], aside [type="password"] {
        margin-top: 1.2vw;
        padding: 1vw;
        border-radius: 20px;
        border: 1px solid #e6e6e6;
    }
    
    /* Botões */
    
    .login-btn {
        margin-top: 2.5vw;
        font-size: .9vw;
        justify-content: space-between;
    }
    
    .login-btn input {
        padding: .8vw 2vw;
        background-color: #00a7aa;
        border-radius: 30px;
        transition: .3s;
    }
    
    .login-btn input:hover {
        background-color: #00c0c4;
    }
    
    .login-btn a {
        color: #00a7aa;
        margin-top: .8vw;
        text-decoration: none;
    }
    
    .login-btn a:hover {
        text-decoration: underline;
        color: #008183;
        text-decoration-thickness: 1.5px;
    }
    
    /* Imagem animada */
    
    article img {
        width: 28vw;
    }
    
    
    /* Modal */
    
    .modal-content {
        box-shadow: 1px 1px 12px 6px rgba(0, 0, 0, 0.274);
    }
    
    .modal-content {
        text-align: start;
    }
    
    
    /* Tabela dos pais */
    
    .table-btn {
        margin-left: 60vw;
        cursor: pointer;
        background-color: #00a7aa;
        transition: .3s;
    }
    
    .table-btn:hover {
        background-color: #019092;
    }
    
    .bg-table-thead {
        background-color: #00a7aa;
    }
    
    .modal-footer button {
        width: 17vw;
        font-size: 1vw;
    }


    /* Tela do(a) professor(a) */
    
    .main-prof {
        margin-top: 8vw;
    }

    .main-prof button {
        background-color: #00a7aa;
    }

    .main-prof button:hover {
        background-color: #009092;
    }

    .main-prof .accordion-button {
        background-color: white;
        border: 1px solid #00a7aa;
        color: #00a7aa;
        transition: .3s;
    }

    .main-prof .accordion-button:hover {
        background-color: #00babd4d;
        color: white;
        border-color: #00babd4d;
    }

    
    /* ESTILIZAÇÃO DO MENÚ RESPONSIVO */
    
    @media (max-width: 991.98px) {
    
        /* Título "Todos Por Um" */
    
        .navbar-brand h1 {
            font-size: 5vw;
            line-height: 4.2vw;
        }
    
        /* Botão "hambúrguer" do menu responsivo */
    
        .navbar-toggler {
            background-color: #00a7aa;
        }
    
        /* Opções do menú: "Início", "Serviços", etc... */
    
        nav ul {
            width: 35%;
            margin: 5vw auto 0px auto;
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
    
        /*
        aside p {
            line-height: 3.8vw;
            font-size: 2.5vw;
        }
        */
    
        .login-inputs {
            font-size: 4vw;
            margin-top: 2vw;
        }
    
        aside input[type="email"], aside input[type="password"] {
            padding: 3vw;
            margin-top: 4vw;
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
    
    
        /* Modal de cadastro dos pais */
    
        .modal-content {
            width: 90vw;
            box-shadow: none;
        }
    
        .modal-body p {
            font-size: 3vw;
        }
    
        .def-fisica, .def-intel {
            font-size: 3.5vw;
        }
    
        .modal-footer button {
            font-size: 3.5vw;
            width: 65vw;
        }
    
        .tamanho-input-modal {
            width: 100%;
        }
    
        .coluna {
            flex-direction: column;
        }
    
        /* Modal do cadastro do aluno */
    
        .modal-content {
            width: 85vw;
        }
    
        .table-btn {
            display: block;
            font-size: 3.2vw;
            margin: auto;
        }
    }
</style>