<template>
  <div class="main">
    <Header/>
    <main>
      <div class="container"><h1>Контент</h1></div>

      <SectionComponent
          v-for="(item, key) in sections"
          :key="key"
          :img="item.img"
          :content="item.content"
          :heading="item.heading"
          :list="item.list"
          :id="item.id"/>
      <div class="container"><ToDo/></div>
    </main>
    <footer>
<div class="container">
  <div>
  <h3>Тыртычный В. А.</h3>
  <h3>201-322</h3>
  <h3>01.06.2021</h3>
  </div>
</div>
    </footer>
  </div>
</template>

<script>
import Header from "../components/Header";
import SectionComponent from "../components/SectionComponent";
import ToDo from "../components/ToDo";

export default {
  name: "Main",
  components: {Header, SectionComponent, ToDo},
  data() {
    return {
      sections: [
        {
          img: 'https://miro.medium.com/max/1200/1*bE_2uKdxR7V9UUSQ-hNhgQ.png',
          heading: 'CSS фреймворки',
          content: '',
          list: ['Tailwind', 'Bootstrap', 'Materialize'],
          id: 'CSS-frameworks'
        },
        {
          img: 'https://miro.medium.com/max/1400/1*yQMlZSgr9xhSLAha_XMHIA.png',
          heading: 'CSS препроцессоры',
          content: 'CSS препроцессор (CSS preprocessor) - это программа, которая имеет свой собственный синтаксис, но может сгенерировать из него CSS код .',
          list: ['Less', 'Sass', 'Stylus'],
          id: 'CSS-preproccessors'
        },
        {
          img: 'https://webformyself.com/wp-content/uploads/2019/31/1.png',
          heading: 'Фреймворки JavaScript',
          content: 'В этой подборке рассмотрены 3 удобных фреймворков для фронтенда.',
          list: ['Vue', 'Angular', 'React'],
          id: 'JS-frameworks'
        }
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
footer div{
  grid-column: 1/-1;
  display: flex;
  justify-content: center;
  flex-direction: column;
  h3{
    text-align: center;
  }
}
</style>