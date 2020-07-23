<template>
  <div id="home-page">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <VtButton class="bg-red-500">This is a button components</VtButton>
    <VtButton class="bg-green-500">This is a button components</VtButton>
    <VtButton class="bg-blue-500">This is a button components</VtButton>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import VtButton from '@elements/VtButton'

export default {
  name: 'home',
  components: {
    HelloWorld,
    VtButton
  },
  mounted () {
    console.log(this)
    this.$store.dispatch('user/read')
  }

}
</script>
