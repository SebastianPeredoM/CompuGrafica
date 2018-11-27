<template lang="pug">
  #app
    template(v-for="seccion in secciones")
      .mdl-card(class="mdl-shadow--2dp")
        .mdl-card__title
          h2(class="mdl-card__title-text") {{ seccion.titulo }}
        .mdl-card__supporting-text
          ul(class="mdl-list")
            li(v-for="item in seccion.items" class="mdl-list__item")
              a(:href="item.url" clas="mdl-list__item-primary-content") {{ item.desc }}
      
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
            },
            {
              desc: 'Animacion',
              url : '../src/pages/Animation.html'
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
