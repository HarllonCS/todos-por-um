<template>

    <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">

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

            <!-- Botão para cadastrar aluno -->
            <button type="button" class="table-btn float-right pt-2 px-2 mt-5 rounded border-0" data-bs-toggle="modal" data-bs-target="#alunoCadastro" title="Cadastrar novo(a) aluno(a)">
                    <span class="material-icons text-light">add</span>
            </button> <!-- /fim do Botão para cadastrar aluno -->

            <!-- Modal -->
            <div class="modal fade" id="alunoCadastro" tabindex="-1" aria-labelledby="labelEstatico" aria-hidden="true" data-bs-backdrop="static" data-bs-keyboard="false">
                <div class="modal-dialog modal-dialog-centered modal-dialog-scrollable">
                    <div class="modal-content mx-auto">
                        <!-- Cabeçalho do Modal -->
                        <div class="modal-header">
                            <!-- Título -->
                            <h5 class="modal-title fw-bold" id="labelEstatico">CADASTRO DO ALUNO</h5> <!-- /fim Título -->
                            
                            <!-- Botão de fechar no canto superior -->
                            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                            <!-- /fim Botão de fechar no canto superior -->
                        </div>  <!-- /fim Cabeçalho do Modal -->
                        
                        <!-- Corpo do Modal -->
                        <div class="modal-body">
                            
                            <p class="mb-4">
                                <small class="text-danger">*</small>
                                <span class="text-secondary">Preenchimento obrigatório</span>
                            </p>

                            <!-- Formulário de cadastro -->
                            <form action="">

                                <!-- Nome e Sobrenome do aluno -->
                                <div class="row cadastro-aluno coluna mb-3">
                                    <div class="col">
                                        <label for="idNome" class="form-label">Nome:</label>
                                        <small class="text-danger">*</small>

                                        <input type="text" class="form-control" id="idNome" required>
                                    </div>

                                    <div class="col">
                                        <label for="idSobrenome" class="form-label">Sobrenome:</label>
                                        <small class="text-danger">*</small>

                                        <input type="text" class="form-control" id="idSobrenome" required>
                                    </div>
                                </div>  <!-- /fim Nome e Sobrenome do aluno -->

                                <div class="row mb-4">
                                <!-- Data de nascimento -->
                                    <div class="col">
                                        <label for="idData">Data de nascimento:</label>
                                        <small class="text-danger">*</small>

                                        <input type="date" id="idData" class="form-control" required>
                                    </div>  <!-- /fim Data de Nascimento -->

                                    <div class="col">
                                        <p>
                                            Sexo:
                                            <small class="text-danger">*</small>
                                        </p>

                                        <div class="form-check form-check-inline">
                                            <input type="radio" class="form-check-input" name="sexo" id="idMasc" value="opt1">

                                            <label for="idDMasc" class="form-check-label">Masculino</label>
                                        </div>

                                        <div class="form-check form-check-inline">
                                            <input type="radio" class="form-check-input" name="sexo" id="idFem" value="opt2" checked>

                                            <label for="idFem" type="radio" class="form-check-label">Feminino</label>
                                        </div>

                                    </div>
                                </div>

                                <!-- Tipo sanguíneo -->
                                <div class="row coluna mb-4">
                                    <div class="col">
                                        <label for="idSangue">Tipo sanguíneo:</label>

                                        <select id="idSangue" class="form-select text-center">
                                            <option value="SemInfo" selected>-- Não sei --</option>

                                            <option value="Amais">A+</option>
                                            <option value="Amenos">A-</option>

                                            <option value="Bmais">B+</option>
                                            <option value="Bmenos">B-</option>

                                            <option value="ABmais">AB+</option>
                                            <option value="ABmenos">AB-</option>

                                            <option value="Omais">O+</option>
                                            <option value="Omenos">O-</option>
                                        </select>
                                    </div> <!-- /fim Tipo sanguíneo -->

                                    <!-- Deficiência(s) (Sim/Não) -->
                                    <div class="col ms-2">
                                        <p>
                                            Possui deficiência:
                                            <small class="text-danger">*</small>
                                        </p>
                                    
                                        <div class="form-check form-check-inline">
                                            <input type="radio" class="form-check-input" name="def" id="idDefSim" value="opt1" checked>

                                            <label for="idDefSim" class="form-check-label">Sim</label>
                                        </div>

                                        <div class="form-check form-check-inline">
                                            <input type="radio" class="form-check-input" name="def" id="idDefNao" value="opt2">

                                            <label for="idDefNao" type="radio" class="form-check-label">Não</label>
                                        </div>
                                    </div>  <!-- /fim Deficiências (Sim/Não) -->
                                </div>

                                <!-- Escolher deficiência(s) -->
                                <div class="mb-4">
                                    <p>Qual(s) deficiência(s):</p>

                                    <div class="d-flex">
                                        <!-- Deficiência físicas -->
                                        <div class="col">
                                            <p class="fw-bold">Física</p>

                                            <div class="form-check mb-1">
                                                <input class="form-check-input" type="checkbox" id="idCheckFis1">

                                                <label class="form-check-label" for="idCheckFis1">Auditiva</label>
                                            </div>

                                            <div class="form-check mb-1">
                                                <input class="form-check-input" type="checkbox" id="idCheckFis2">

                                                <label class="form-check-label" for="idCheckFis2">Visual</label>
                                            </div>

                                            <div class="form-check mb-1">
                                                <input class="form-check-input" type="checkbox" id="idCheckFis3">

                                                <label class="form-check-label" for="idCheckFis3">Paraplegia</label>
                                            </div>

                                            <div class="form-check mb-1">
                                                <input class="form-check-input" type="checkbox" id="idCheckFis4">

                                                <label class="form-check-label" for="idCheckFis4">Monoplegia</label>
                                            </div>

                                            <div class="form-check mb-1">
                                                <input class="form-check-input" type="checkbox" id="idCheckFis5">

                                                <label class="form-check-label" for="idCheckFis5">Tetraplegia</label>
                                            </div>

                                            <div class="form-check mb-1">
                                                <input class="form-check-input" type="checkbox" id="idCheckFis6">

                                                <label class="form-check-label" for="idCheckFis6">Hemiplegia</label>
                                            </div>

                                            <div class="form-check mb-1">
                                                <input class="form-check-input" type="checkbox" id="idCheckFis7">

                                                <label class="form-check-label" for="idCheckFis7">Ostomia</label>
                                            </div>

                                            <div class="form-check mb-1">
                                                <input class="form-check-input" type="checkbox" id="idCheckFis8">

                                                <label class="form-check-label" for="idCheckFis8">Paralisia cerebral</label>
                                            </div>
                                        </div> <!-- /fim Deficiências físicas -->
                                        
                                        <!-- Deficiências intelectuais -->
                                        <div class="col">
                                            <p class="fw-bold">Intelectual</p>

                                            <div class="form-check mb-1">
                                                <input class="form-check-input" type="checkbox" id="idCheckInt1">

                                                <label class="form-check-label" for="idCheckInt1">Autismo Leve</label>
                                            </div>

                                            <div class="form-check mb-1">
                                                <input class="form-check-input" type="checkbox" id="idCheckInt2">

                                                <label class="form-check-label" for="idCheckInt2">Autismo Moderado</label>
                                            </div>

                                            <div class="form-check mb-1">
                                                <input class="form-check-input" type="checkbox" id="idCheckInt3">

                                                <label class="form-check-label" for="idCheckInt3">Autismo Grave</label>
                                            </div>

                                            <div class="form-check mb-1">
                                                <input class="form-check-input" type="checkbox" id="idCheckInt4">

                                                <label class="form-check-label" for="idCheckInt4">Síndrome de Down</label>
                                            </div>
                                        </div> <!-- /fim Deficiências intelectuais -->
                                    </div>
                                </div> <!-- /fim Escolher deficiência(s) -->

                                <div class="row coluna">
                                    <div class="col">
                                        <p>
                                            Turma:
                                            <small class="text-danger">*</small>
                                        </p>

                                        <select class="form-select" required>
                                            <optgroup label="Turma A">
                                                <option value="ano1A">1º Ano - A</option>
                                                <option value="ano2A">2º Ano - A</option>
                                                <option value="ano3A">3º Ano - A</option>
                                                <option value="ano4A">4º Ano - A</option>
                                            </optgroup>

                                            <optgroup label="Turma B">
                                                <option value="ano1B">1º Ano - B</option>
                                                <option value="ano2B">2º Ano - B</option>
                                                <option value="ano3B">3º Ano - B</option>
                                                <option value="ano4B">4º Ano - B</option>
                                            </optgroup>
                                        </select>
                                    </div> <!-- /fim Turma do aluno -->

                                    <!-- Turno do aluno -->
                                    <div class="col ms-2">
                                        <p>
                                            Turno:
                                            <small class="text-danger">*</small>
                                        </p>

                                        <div class="form-check form-check-inline">
                                            <input type="radio" id="idManha" class="form-check-input" name="radioTurno" checked>
                                            <label for="idManha" class="form-check-label">Manhã</label>
                                        </div>

                                        <div class="form-check form-check-inline">
                                            <input type="radio" id="idTarde" class="form-check-input" name="radioTurno">
                                            <label for="idTarde" class="form-check-label">Tarde</label>
                                        </div>

                                        <div class="form-check form-check-inline">
                                            <input type="radio" id="idIntegral" class="form-check-input" name="radioTurno">
                                            <label for="idIntegral" class="form-check-label">Integral</label>
                                        </div>
                                    </div> <!-- /fim Turno do aluno -->
                                </div>
                            </form> <!-- /fim Formulário de cadastro -->
                        </div> <!-- /fim Corpo do Modal -->
                        
                        <!-- Rodapé do Modal -->
                        <div class="modal-footer">
                            
                            <!-- Botão de Enviar -->
                            <button type="button" class="btn btn-success fw-bold mx-auto w-75">
                                ENVIAR
                            </button> <!-- /fim Botão de Enviar -->
                        </div> <!-- /fim Rodapé do Modal -->
                    </div>
                </div>
            </div> <!-- /fim Modal -->

            <main role="main">
                <!-- Tabela de alunos acadastrados (pais ou responsáveis) -->
                <table class="table table-striped table-bordered table-hover w-75 mx-auto text-center shadow">
                    <!-- Cabeçalho da tabela -->
                    <thead class="bg-table-thead text-light">
                        <th scope="col">ID</th>
                        <th scope="col">NOME</th>
                        <th scope="col">ANO E TURMA</th>
                        <th scope="col">TURNO</th>
                        <th scope="col">AÇÃO</th>
                    </thead> <!-- /fim do Cabeçalho da tabela -->

                    <tbody> <!-- Corpo da tabela -->
                        <tr>
                            <th scope="row">1</th>
                            <td>Fulano</td>
                            <td>9º C</td>
                            <td>Tarde</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Deletar">delete</span>
                                    <span class="material-icons" title="Editar">edit</span>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <th scope="row">2</th>
                            <td>Ciclano</td>
                            <td>7º B</td>
                            <td>Manhã</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Deletar">delete</span>
                                    <span class="material-icons" title="Editar">edit</span>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <th scope="row">3</th>
                            <td>Beutrano</td>
                            <td>6º A</td>
                            <td>Integral</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Deletar">delete</span>
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
        text-align: start;
    }
    
    .modal-dialog {
        max-width: 35vw;
    }
    
    /* Tabela */
    
    table {
        font-size: 1vw;
    }

    table span {
        cursor: pointer;
    }

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