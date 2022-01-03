<template>
        <div>
            <Picture />

            <p v-if="estou_trabalhando">Estou trabalhando no momento.</p>
            <p v-else>Estou aberto a novas oportunidades.</p>
            <p>Utilizo as seguintes tecnologias de Back-end:</p>
            <ul>
                <li v-for="(tecnologiaBe, index) in backEnd" v-bind:key="index">{{ tecnologiaBe }}</li>
            </ul>

            <p>Utilizo as seguintes tecnologias de Front-end:</p>
            <ul>
                <li v-for="tecnologiaFe in frontEnd" :key="tecnologiaFe.id">{{ tecnologiaFe.language }}</li>
            </ul>

            <button @click="mostrarEmail">{{ textoBtn }}</button>

            <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>

            <p>Para mais informacoes, acesse esse link: <a v-bind:href="meu_link" target="_blank">Meu Link</a></p>
    </div>
</template>

<script>
    import Picture from "./Picture.vue"

    export default {
        name: 'Info',
        components: {
            Picture
        },
        data() {
            return {
                estou_trabalhando: true,
                mostrar_email: false,
                email: 'isaacelias1110@gmail.com',
                meu_link: 'https://www.google.com',
                textoBtn: "Mostrar Email",
                backEnd: ['Python', 'PHP', 'Java', 'Asp.Net'],
                frontEnd: [
                    {
                        id: 1, language: 'HTML'    
                    },
                    {
                        id: 2, language: 'CSS'
                    },
                    {
                        id: 3, language: 'Vue'
                    }
                ]
            }
        },

        methods: {
            mostrarEmail() {
                this.mostrar_email = !this.mostrar_email
                switch (this.textoBtn) {
                    case "Mostrar Email":
                        this.textoBtn = "Ocultar Email"
                        break;
                
                    default:
                        this.textoBtn = "Mostrar Email"
                        break;
                }
            }
        }
    }
</script>
