<template>
    <div class="jumbo">
    </div>
</template>

<script>
    export default {
        name: 'ContentJumbo'
    }
</script>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    .jumbo{
        background-image: url(../assets/img/jumbotron.jpg);
        height: 400px;
    }
</style>