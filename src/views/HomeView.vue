<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>

    <FormContact/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import FormContact from '@/components/FormContact.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    FormContact
}
}
</script>
