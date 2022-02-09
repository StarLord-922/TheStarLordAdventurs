<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <Suspense>
      <template #default>
    <MyHome />
      </template >
      <template #fallback>
        loading ...
      </template>
    </Suspense>
  </div>
  
</template>

<script>
// @ is an alias to /src
import MyHome from '@/components/MyHome.vue'

export default {
  name: 'Home',
  components: {
    MyHome
  }
}
</script>
