<template>
       <h3>This is my list</h3>
             <h4>{{user.first_name}} {{user.last_name}}</h4>
</template>

<script>


export default {
        name:"User",
      props:{
         user:Object
    }
}
</script>

<style scoped>

</style>>

