<template>
    <div>
        <Reutilizacao />
        <h1>Olá Vue!</h1>
        <h3>Me chamo {{ nome }}, e sou {{ profissao }}</h3>
        <Reutilizacao />
        <MultiplosEventos />

        <Reutilizacao />
    </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue'
import Reutilizacao from './Reutilizacao.vue'

export default {
    name: 'primeiroComponente',
    components: {
        MultiplosEventos,
        Reutilizacao
    },
     data() {
         return {
             nome: "Isaac",
             profissao: "Desenvolvedor Front-end"
         }
     }
}
</script>