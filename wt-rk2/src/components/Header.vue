<template>
    <header>
      <div class="container">
        <div class="header">
        <div class="header-logo"><img  alt="Логотип"
                                      srcset="../assets/imgs/logo-32.png 1x, ../assets/imgs/logo-64.png 2x">
        </div>
        <nav class="header-nav">
          <div class="header-nav__item"><a href="#CSS-frameworks">CSS фреймворки</a></div>
          <div class="header-nav__item"><a href="#CSS-preproccessors">CSS препроцессоры</a></div>
          <div class="header-nav__item"><a href="#JS-frameworks">Фреймворки JavaScript</a></div>
        </nav>
        <button class="header-theme-switcher">Сменить тему</button>
      </div>
      </div>
    </header>
</template>

<script>
export default {
  name: "Header",
}
</script>

<style lang="scss" scoped>

</style>