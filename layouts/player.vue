<template>
    <div id="app">
        <nav-bar />
        <h3>nba player</h3>
        <div>this page will show nba player infomation</div>
        <nuxt />
    </div>
</template>

<script>
import NavBar from "~/components/NavBar.vue";
export default {
    components:{
        NavBar
    }
};
</script>