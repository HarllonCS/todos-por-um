<template>

<main role="main">

</main>
</template>

<script>

    export default {
        name: "Salas"
    }

</script>

<style>

    /* Formatação do Cabeçalho (logo) */
    .navbar-brand span {
        color: #00a7aa;
    }

    /* Tela do(a) professor(a) */
    .d-grid button {
        background-color: #00a7aa;
        margin-bottom: 1.3vw;
        transform: .3s;
    }

    .d-grid button:hover {
        background-color: #009092;
    }

    @media (min-width: 576px) and (max-width: 767.98px) {
        .d-grid button {
            margin-bottom: 4vw;
        }
    }
</style>