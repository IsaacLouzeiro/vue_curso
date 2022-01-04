<template>
    <img v-bind:src="avatar" :alt="descricao">

    <MudarImagem @mudar-imagem="alterarImagem" class="mudarImagem" />
</template>

<script>
import MudarImagem from './MudarImagem.vue'

export default {
    name: 'Picture',
    components: {
        MudarImagem
    },
    data() {
        return {
            avatar: "/img/avatar.png",
            descricao: "Avatar do usuário"
        }
    },
    methods: {
        alterarImagem() {
            switch (this.avatar) {
                case "/img/avatar.png":
                    this.avatar = "/img/avatar2.png"
                    break;
                case "/img/avatar2.png":
                    this.avatar = "/img/avatar.png"
                    break;
            
                default:
                    break;
            }
        }
    }
}
</script>

<style scoped>
img {
    width: 150px;
}
.mudarImagem {
    display: block;
    padding: 5px 10px;
    margin: 10px;
    cursor: pointer;
}
</style>