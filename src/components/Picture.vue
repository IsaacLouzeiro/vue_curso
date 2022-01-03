<template>
    <img v-bind:src="avatar" :alt="descricao">
</template>

<script>
export default {
    name: 'Picture',
    data() {
        return {
            avatar: "/img/avatar.png",
            descricao: "Avatar do usuário"
        }
    }
}
</script>