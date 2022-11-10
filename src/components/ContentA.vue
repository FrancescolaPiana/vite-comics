<template>
    <div class="principal">
        <div class="container">
            <h2> -> Content goes HERE  </h2>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'ContentA',
    }
</script>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    .principal{
        background-color: $darkgrey;
        padding: 3rem 0rem;
        .container{
            max-width: 1170px;
            margin: 0 auto ;
            h2{
                color: white;
            }
        }
    }
</style>