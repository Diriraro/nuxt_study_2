<template>
  <div class="container">
    <header>
      <h1 class="title">{{title}}</h1>
      <img src="https://miro.medium.com/max/750/1*NTGKGfvCt9bX_S8qqCBgBQ.png" alt="" />
      <nav>
        <nuxt-link to="/services">HELLO WWWOOOORRRRLLLDD </nuxt-link>
      </nav>
    </header>
    <nuxt-link to="/one" target="_blank" class="button--green">
      documentation
    </nuxt-link>
    <nuxt-link to="/two" target="_blank" class="button--green">
      documentation
    </nuxt-link>
    <nuxt-link to="/three" target="_blank" class="button--green">
      documentation
    </nuxt-link>
  </div>
</template>

<script>
export default {
  data(){
    return{
      title : 'Nuxt.js를 활용한 서버사이드렌더링이래'
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
