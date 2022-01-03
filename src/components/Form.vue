<template>
    <form action="" @submit="enviarForm($event)">
        <h2>Meu formulário: </h2>
        <div>
            <input type="text" v-model="name">
        </div>
        <div>
            <input type="text" v-model="email">
        </div>
        <div>
            <InputSubmit />
        </div>
    </form>
</template>

<script>
import InputText from './InputText.vue'
import InputSubmit from './InputSubmit.vue'

export default {
    name: 'Form',
    components: {
        InputText,
        InputSubmit
    },
    data() {
        return {
            name: '',
            email: ''
        }
    },
    methods: {
        enviarForm(e) {
            e.preventDefault();

            const name = this.name;
            const email = this.email;

            alert('Formulário Enviado')
            alert(`Olá ${name}, irei enviar as novidades para o email ${email}. Até breve!`)
        }
    }
}
</script>