<template>
  <section class="education">
    <div class="timeline">

      <div class="container">
        <h2>Bacharelado em TI <h4>2021 - Atual</h4></h2>
        <h2>Universidade Federal do Rio Grande do Norte (UFRN)</h2>
      </div>

      <div class="container">
        <h2>Curso Técnico em Eletrônica <h4>2017 - 2021</h4></h2>
        <h2>Instituto Federal do Rio Grande do Norte (IFRN)</h2>
      </div>

    </div>
  </section>
</template>

<script>
export default {
  name: 'Education',
  data: function(){
      return {
          
      }
  }
}
</script>

<style scoped>
.education{
  padding: 20px;
  min-height: 600px;
  position: relative;
}
.timeline {
  width: 100%;
  height: 600px;
  position: relative;
  margin: 0 auto;

  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}
.timeline::after {
  content: '';
  position: absolute;
  width: 6px;
  background-color: var(--color-warning);
  top: 0;
  bottom: 0;
  left: 200px;
  margin-left: -3px;
}
.container {
  background-color: var(--color-background-dark);
  color: var(--color-background);
  position: relative;
  left: 300px;
  width: 900px;
  height: 200px;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: left;
}
.container::before{
  content: " ";
height: 0;
position: absolute;
top: 22px;
width: 0;
z-index: 1;
left: -10px;
border: medium solid var(--color-background-dark);
border-width: 10px 10px 10px 0;
border-color: transparent var(--color-background-dark) transparent transparent;
}

.container::after{
  content: '';
  position: absolute;
  width: 16px;
  height: 16px;
  left: -113px;
  background-color: var(--color-background-dark);
  border: 4px solid var(--color-warning);
  top: 15px;
  border-radius: 50%;
  z-index: 1;
}

.container h2 {
  font-size: 18px;
}
.container h4 {
  font-size: 13px;
}
</style>
