<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
<<<<<<< HEAD
    <HelloWorld msg="Welcome to Your Vue.js App"/>
=======
    <Suspense>
      <template #default>
    <MyHome />
      </template >
      <template #fallback>
        loading ...
      </template>
    </Suspense>
>>>>>>> parent of 2c042ae... last header modifications
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
