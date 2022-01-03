<template>
  <div>
      <button @click="ativar">Clique aqui!!</button>
      <span v-show="ativado">Ativou!</span>
  </div>
</template>

<script>
export default {
    name: 'Reutilizacao',
    data() {
        return {
            ativado: false
        }
    },
    methods: {
        ativar() {
            this.ativado = !this.ativado
        }
    }
}
</script>

<style scoped>
    span {
        display: block;
        width: 200px;
        background-color: rgb(42, 165, 42);
        color: #fff;
        margin-top: 10px;
        padding: 15px;
        text-align: center;
    }
</style>