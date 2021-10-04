<template>
  <nav class="">
      <ul>
          <li @click="$emit('page',1)" active>Sobre</li>
          <li @click="$emit('page',2)">Formação</li>
          <li @click="$emit('page',3)">Portfolio</li>
          <li @click="$emit('page',1)">Contato</li>
      </ul>
  </nav>
</template>

<script>
export default {
  name: 'Nav',
  methods: {
      click( n ){
          this.$emit('page',n )
      }
  }
}
</script>

<style scoped>
nav {
    width: 100%;
    background-color: var(--color-primary);
    color: var(--color-text);
    height: 50px;
    font-size: 18px;
}
nav ul {
    display: flex;
    justify-content: space-around;
    height: 100%;
    list-style: none;
}
nav ul li {
    height: 100%;
    min-width: 80px;
    display: flex;
    align-items: center;
    justify-content: center;
}
nav ul li[active] {
    border-top: 3px solid var(--color-text);
    border-bottom: 3px solid var(--color-text);
}
</style>
