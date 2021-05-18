<template>
  <!-- <div class="container">
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
  </div> -->
  <section class="container">
    <ul>
      <li v-for="item in todos" :key="item.id">
        <input type="checkbox" :checked="item.done" @change="toggle(item)" />
        <span :class="{done: item.done}"> {{item.title}} </span>
        <button @click="remove(item)">지우기</button>
      </li>
    </ul>
    <p> 
      <input type="text" placeholder="할 일을 적으셈" v-model="todoTitle" @keyup.enter="addTodo" /> 
      <button @click="addTodo">입력</button> 
    </p>
  </section>
</template>

<script>
import {mapMutations} from 'vuex';
export default {
  // data(){
  //   return{
  //     title : 'Nuxt.js를 활용한 서버사이드렌더링이래'
  //   }
  // }
  // ---------------------------------------------------------------------------------------
  data: function(){
    return{
      todoTitle: '',
    };
  },
  computed: {
    todos (){
      return this.$store.state.todo.list;
    }
  },
  methods :{
    addTodo (){
      this.$store.commit('todo/add', this.todoTitle);
      this.todoTitle = '';
    },
    ...mapMutations({
      toggle: 'todo/toggle',
      remove: 'todo/remove'
    })
  }

}
</script>

<style>
.done { text-decoration: line-through; }
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
