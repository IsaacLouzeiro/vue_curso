<template>
    <button @click="$emit('mudarImagem')">Mudar imagem</button>
</template>

<script>
export default {
    name: 'MudarImagem',
    emits: ['mudarImagem']
}
</script>