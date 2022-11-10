<template>
 <HeaderC/>

 <main>
 <ContentA/>
 <ContentLinks/>
 <ContentLists/>
 </main>

 <FooterC/>
</template>

<script>
  import HeaderC from './components/HeaderC.vue';
  import ContentA from './components/ContentA.vue';
  import ContentLinks from './components/ContentLinks.vue';
  import ContentLists from './components/ContentLists.vue';
  import FooterC from './components/FooterC.vue';


  export default {
    components: {
      HeaderC,
      ContentA,
      ContentLinks,
      ContentLists,
      FooterC
    }
  }
</script>

<style lang="scss" scoped>
</style>