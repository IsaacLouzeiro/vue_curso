<template>
    <div>
        <h2>Esta é a descricao da pessoa: {{ nome }}</h2>

        <Info :email="email" :estou_trabalhando=false />
    </div>
</template>

<script>
    import Info from './Info.vue'
    
    export default {

        name: 'Pessoa',
        components: {
            Info
        },
        data() {
            return {
                nome: 'Isaac',
                email: 'isaacelias@email.com'
            }
        }
    }
</script>