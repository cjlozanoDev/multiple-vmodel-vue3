<template>
  <article class="content">
    <form class="form">
      <div class="control">
        <label for="name"> Nombre </label>
        <input
          :value="name"
          @input="event => $emit('update:name', event.target.value)"
          type="text"
          id="name"
          placeholder="Escribe tu nombre"/>
      </div>

      <div class="control">
        <label for="name"> Edad </label>
        <input
          :value="age"
          @input="event => $emit('update:age', event.target.value)"
          type="number"
          id="age"
          placeholder="Escribe tu edad"/>
      </div>

      <div class="control">
        <label for="colour"> Color favorito </label>
        <input
          :value="color"
          @input="event => $emit('update:color', event.target.value)"
          type="color"
          id="color"
          placeholder="Selecciona tu color favorito"/>
      </div>
    </form>
  </article>

</template>

<script>
export default {
  name: 'PersonalForm',
  props: ['name', 'color', 'age']
}
</script>