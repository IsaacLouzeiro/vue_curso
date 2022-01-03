<template>
    <div>
        <h2>Aula sobre {{ nome }}</h2>
    </div>
</template>

<script>
export default {
    name: 'LifeCycle',
    data() {
        return {
            nome: 'Não definido'
        }
    },
    created() {
        this.nome = 'Ciclo de Vida 1'
    },

    mounted() {
        setTimeout(() => {
            this.nome = 'Ciclo de Vida 2'
        }, 1000)
    }
}
</script>