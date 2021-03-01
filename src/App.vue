<template>
  <article :style="{ backgroundColor: color }">
    <img alt="Vue logo" src="./assets/logo.png" />
    <!-- <PersonalForm
      :name="name"
      :age="age"
      :color="color"
      @update:name="updateName"
      @update:age="updateAge"
      @update:color="updateColor"/> -->

    <PersonalForm
      :name="name"
      :age="age"
      :color="color"
      v-model:name="name"
      v-model:age="age"
      v-model:color="color"/>
   </article>
</template>

<script>
import { ref } from 'vue'
import PersonalForm from './components/PersonalForm.vue'

export default {
  name: 'App',
  components: {
    PersonalForm
  },
  setup() {
    const name = ref('John Doe')
    const age = ref(33)
    const color = ref('#FF0000')
    
    return { name, age, color}
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>