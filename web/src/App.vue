<template lang="pug">
  #app
    template(v-for="seccion in secciones")
      label {{ seccion.titulo }}
      ul
        li(v-for="item in seccion.items")
          a(:href="item.url") {{ item.desc }}
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      secciones: [
        {
          titulo: 'Laboratorio',
          items : [
            {
              desc: 'Inicio',
              url : '../src/pages/index.html'
            },
            {
              desc: 'Escalera',
              url : '../src/pages/Escaleras.html'
            },
            {
              desc: 'Banquito',
              url : '../src/pages/Banquito.html'
            },
            {
              desc: 'Perfumes',
              url : '../src/pages/Perfumes.html'
            }
          ]
        },
        {
          titulo: 'Ejercicios',
          items : [
            {
              desc: 'Computadora v0.1',
              url : '../src/pages/Computadora.html'
            },
            {
              desc: 'Laptop v0.1',
              url : '../src/pages/Laptop.html'
            }            
          ]
        },
        {
          titulo: 'Castito',
          items : [
            {
              desc: 'Dispensador de agua',
              url : '../src/pages/DispensadorCafe.html'
            }
          ]
        }
      ]
    }
  }
}
</script>

<style lang="scss">

</style>
