<template>

  <div>
    <PrimeiroComponente />
    <LifeCycle />
    <Pessoa />
    <Form />
    <Counter />
  </div>

</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'
import Form from './components/Form.vue'
import Counter from './components/Counter.vue'

export default {
  name: 'App',
  components: {
    PrimeiroComponente,
    LifeCycle,
    Pessoa,
    Form,
    Counter
  }
}
</script>

<style scoped>
  * {
    margin: 0;
    padding: 0;  
  }
</style>