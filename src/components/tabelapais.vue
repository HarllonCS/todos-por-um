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

            <!-- Botão para cadastrar aluno -->
            <button type="button" class="table-btn float-right pt-2 px-2 mt-5 rounded border-0" data-bs-toggle="modal" data-bs-target="#alunoCadastro" title="Cadastrar novo(a) aluno(a)">
                    <span class="material-icons text-light">add</span>
            </button> <!-- /fim do Botão para cadastrar aluno -->

            <!-- Modal -->
            <div class="modal fade" id="alunoCadastro" tabindex="-1" aria-labelledby="labelEstatico" aria-hidden="true" data-bs-backdrop="static" data-bs-keyboard="false">
                <div class="modal-dialog modal-dialog-centered modal-dialog-scrollable mx-auto">
                    <div class="modal-content">
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
                                            <input type="radio" class="form-check-input" name="def" id="idDefSim" value="opt1">

                                            <label for="idDefSim" class="form-check-label">Sim</label>
                                        </div>

                                        <div class="form-check form-check-inline">
                                            <input type="radio" class="form-check-input" name="def" id="idDefNao" value="opt2" checked>

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

            <main role="main" class="overflow-auto mx-auto border border-2">
                <!-- Tabela de alunos acadastrados (pais ou responsáveis) -->
                <table class="table table-striped table-bordered text-center">
                    <!-- Cabeçalho da tabela -->
                    <thead class="text-light">
                        <th scope="col">ID</th>
                        <th scope="col">NOME</th>
                        <th scope="col">TURMA</th>
                        <th scope="col">TURNO</th>
                        <th scope="col"></th>
                    </thead> <!-- /fim do Cabeçalho da tabela -->

                    <tbody> <!-- Corpo da tabela -->
                        <tr>
                            <td>1</td>
                            <td>Fulano</td>
                            <td>1º A</td>
                            <td>Tarde</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Editar" type="button" data-bs-target="#editModal" data-bs-toggle="modal">edit</span>

                                    <span class="material-icons" title="Deletar">delete</span>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>2</td>
                            <td>Ciclano</td>
                            <td>2º B</td>
                            <td>Manhã</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Editar" type="button" data-bs-target="#editModal" data-bs-toggle="modal">edit</span>

                                    <span class="material-icons" title="Deletar">delete</span>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>3</td>
                            <td>Beutrano</td>
                            <td>3º A</td>
                            <td>Integral</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Editar" type="button" data-bs-target="#editModal" data-bs-toggle="modal">edit</span>

                                    <span class="material-icons" title="Deletar">delete</span>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>4</td>
                            <td>Zé da Uva</td>
                            <td>4º A</td>
                            <td>Integral</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Editar" type="button" data-bs-target="#editModal" data-bs-toggle="modal">edit</span>

                                    <span class="material-icons" title="Deletar">delete</span>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>5</td>
                            <td>Maracujá</td>
                            <td>3º A</td>
                            <td>Integral</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Editar" type="button" data-bs-target="#editModal" data-bs-toggle="modal">edit</span>

                                    <span class="material-icons" title="Deletar">delete</span>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>6</td>
                            <td>Roliço</td>
                            <td>3º A</td>
                            <td>Integral</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Editar" type="button" data-bs-target="#editModal" data-bs-toggle="modal">edit</span>

                                    <span class="material-icons" title="Deletar">delete</span>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>7</td>
                            <td>Anão</td>
                            <td>1º A</td>
                            <td>Tarde</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Editar" type="button" data-bs-target="#editModal" data-bs-toggle="modal">edit</span>

                                    <span class="material-icons" title="Deletar">delete</span>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>8</td>
                            <td>Beyblade</td>
                            <td>2º B</td>
                            <td>Manhã</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Editar" type="button" data-bs-target="#editModal" data-bs-toggle="modal">edit</span>

                                    <span class="material-icons" title="Deletar">delete</span>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>9</td>
                            <td>Juju</td>
                            <td>3º A</td>
                            <td>Integral</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Editar" type="button" data-bs-target="#editModal" data-bs-toggle="modal">edit</span>

                                    <span class="material-icons" title="Deletar">delete</span>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>10</td>
                            <td>Engraçadinha</td>
                            <td>3º A</td>
                            <td>Integral</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Editar" type="button" data-bs-target="#editModal" data-bs-toggle="modal">edit</span>

                                    <span class="material-icons" title="Deletar">delete</span>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>11</td>
                            <td>Alexius</td>
                            <td>4º B</td>
                            <td>Integral</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Editar" type="button" data-bs-target="#editModal" data-bs-toggle="modal">edit</span>

                                    <span class="material-icons" title="Deletar">delete</span>
                                </div>
                            </td>
                        </tr>

                        <tr>
                            <td>12</td>
                            <td>Careca</td>
                            <td>4º B</td>
                            <td>Integral</td>
                            <td>
                                <div class="d-flex justify-content-around">
                                    <span class="material-icons" title="Editar" type="button" data-bs-target="#editModal" data-bs-toggle="modal">edit</span>

                                    <span class="material-icons" title="Deletar">delete</span>
                                </div>
                            </td>
                        </tr>
                    </tbody> <!-- /fim Corpo da tabela -->
                </table>  <!-- /fim Tabela -->
            </main>

            <div class="modal fade" id="editModal" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1" aria-hidden="true" aria-labelledby="tabelaModal">
                <div class="modal-dialog modal-dialog-scrollable">
                    <div class="modal-content mx-auto">
                        <div class="modal-header">
                            <h5 class="modal-title" id="tabelaModal">Editar dados do(a) aluno(a)</h5>

                            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                        </div>

                        <div class="modal-body">
                            <!-- Formulário de cadastro -->
                            <form action="">
                                <!-- Nome e Sobrenome do aluno -->
                                <div class="row cadastro-aluno coluna mb-3">
                                    <div class="col">
                                        <label for="idNome" class="form-label">Nome:</label>

                                        <input type="text" class="form-control" id="idNome" required>
                                    </div>

                                    <div class="col">
                                        <label for="idSobrenome" class="form-label">Sobrenome:</label>

                                        <input type="text" class="form-control" id="idSobrenome" required>
                                    </div>
                                </div>  <!-- /fim Nome e Sobrenome do aluno -->

                                <div class="row mb-4">
                                <!-- Data de nascimento -->
                                    <div class="col">
                                        <label for="idData">Data de nascimento:</label>

                                        <input type="date" id="idData" class="form-control" required>
                                    </div>  <!-- /fim Data de Nascimento -->

                                    <div class="col">
                                        <p>Sexo:</p>

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
                                        <p>Possui deficiência:</p>
                                    
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
                                        <p>Turma:</p>

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
                                        <p>Turno:</p>

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
                        </div>

                        <div class="modal-footer">
                            <button type="button" class="btn btn-success fw-bold w-75 mx-auto">EDITAR</button>
                        </div>
                    </div>
                </div>
            </div>
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
        font-size: 2.5vw;
        line-height: 2vw;
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

    
    /* Modal */
    
    .modal-content {
        box-shadow: 1px 1px 12px 6px rgba(0, 0, 0, 0.274);
        text-align: start;
    }
    
    .modal-dialog {
        max-width: 35vw;
    }

    .modal-footer button {
        width: 17vw;
        font-size: 1vw;
    }

    
    /* Tabela */

    main {
        height: 47vh;
        width: 40vw;
        box-shadow: 0px 10px 13px 2px rgba(0, 0, 0, 0.274);
    }

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
    
    thead {
        background-color: #00a7aa;
        font-size: 1.3vw;
    }
    
    
    /* ESTILIZAÇÃO RESPONSIVA */
    
    @media (max-width: 767.98px) {
    
        .cont {
            width: 95vw;
        }

        /* Título "Todos Por Um" */
    
        .navbar-brand h1 {
            font-size: 5vw;
            line-height: 4.2vw;
        }


        /* Botão de sair */

        .offcanvas-body button span {
            font-size: 7vw;
        }

        .offcanvas-body button sup {
            font-size: 4vw;
            margin-left: 3vw;
        }


        /* Modal de cadastro dos alunos */
    
        .modal-dialog {
            max-width: 85vw;
            box-shadow: none;
        }
    
        .modal-body p {
            font-size: 5vw;
        }

        label {
            font-size: 4vw;
        }
    
        .modal-footer button {
            font-size: 6vw;
        }
    
        .coluna {
            flex-direction: column;
        }
        

        /* Botão da tabela */
    
        .table-btn {
            display: block;
            margin: auto;
            margin-bottom: 10vw;
        }


        /* Tabela */

        main {
            box-shadow: none;
            width: 98%;
        }

        thead {
            font-size: 5vw;
        }

        table {
            font-size: 3.6vw;
        }
    }

    @media (min-width: 768px) and (max-width: 991.98px) {
        .cont {
            width: 95vw;
        }

        .navbar-brand h1 {
            font-size: 4vw;
            line-height: 3.6vw;
        }

        .list-group {
            font-size: 2.5vw;
        }

        /* Botão da tabela */
    
        .table-btn {
            margin: 0 auto 6vw 0;
        }

        /* Tabela */

        main {
            box-shadow: none;
            width: 98%;
        }

        thead {
            font-size: 3vw;
        }

        table {
            font-size: 2.7vw;
        }

        /* Modal de cadastro dos alunos */
    
        .modal-dialog {
            max-width: 85vw;
            box-shadow: none;
        }

        .container-fluid .perfil {
            font-size: 2.5vw;
        }


        /* Botão de sair */

        .offcanvas-body button span {
            font-size: 3.5vw;
        }

        .offcanvas-body button sup {
            font-size: 2vw;
            margin-left: 3vw;
        }

        /* Modal */

        .modal-footer button {
            font-size: 2.5vw;
        }
    }

    @media (min-width: 992px) and (max-width: 1199.98px) {
        /* Título "Todos Por Um" */

        .navbar-brand h1 {
            font-size: 3.5vw;
            line-height: 2.8vw;
        }

        /* Botão da tabela */
    
        .table-btn {
            margin: 0 auto 3vw 0;
        }

        /* Tabela */

        main {
            box-shadow: none;
            width: 90%;
        }

        thead {
            font-size: 2.5vw;
        }

        table {
            font-size: 2vw;
        }

        /* Botão de sair */

        .offcanvas-body button span {
            font-size: 2.5vw;
        }

        .offcanvas-body button sup {
            font-size: 1.6vw;
            margin-left: 2vw;
        }

        .list-group {
            font-size: 1.8vw;
        }

        /* Modal de cadastro dos alunos */
    
        .modal-dialog {
            max-width: 80vw;
        }

        .modal-footer button {
            font-size: 2vw;
        }
    }

    @media (min-width: 1200px) and (max-width: 1399.98) {
        /* Modal de cadastro dos alunos */
    
        .modal-dialog {
            max-width: 80vw;
        }

        .modal-footer {
            font-size: 5vw;
        }
    }
</style>