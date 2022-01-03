<template>
    <div>
        <h2>Contador </h2>
        <p>{{ numero }}</p>
        <button @click="mais">+</button>
        <button @click="menos">-</button>
    </div>
</template>

<script>
export default {
    name: 'Counter',
    data() {
        return {
            numero: 0
        }
    },
    
    methods: {
        mais() {
            this.numero++
        },
        menos() {
            this.numero--
        }
    }
}
</script>