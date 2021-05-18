<template>
    <div class=" ">
        <nav-bar/>
        <h1>Create An Event</h1>
        <nuxt />
    </div>
</template>
<!-- <script>
export default {
    layout:'create'
}
</script> -->
<script>
import NavBar from "~/components/NavBar.vue";
export default {
    components:{
        NavBar
    }
};
</script>