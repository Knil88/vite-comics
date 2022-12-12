<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default{
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  }
}
</script>

<template>
 
  <AppHeader/>
  <AppMain/>
  <AppFooter/>
</template>

<style lang="scss" >

@use'./components/styles/generals.scss'as*;
@use'./components/styles/partials/variables'as*;
</style>
