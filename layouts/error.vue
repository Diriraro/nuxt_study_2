<template>
    <div class="container">
        <h1 v-if="error.statusCode === 404"> 페이지 업슴</h1>
        <h1 v-else>에러밠객</h1>
        <nuxt-link to="/">홈페이지</nuxt-link>
    </div>
</template>

<script>
export default {
    props: ['error'],
    layout: 'team'
}
</script>