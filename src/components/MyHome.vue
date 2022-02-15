<template>
  <h1>Welcome home</h1>
  <dir>

        
      <AsyncUser />
  </dir>
 
</template>

<script>

import LoadingComponent from "@/components/LoadingComponent.vue"
import ErrorComponent from "@/components/ErrorComponent.vue"
import {defineAsyncComponent} from "vue"

const AsyncUser=defineAsyncComponent({
    loader:()=>import(/*webpackChunkName:"list" */ "./Users.vue"),
    loadingComponent:LoadingComponent,
    error:ErrorComponent,
    suspensible:false
})
export default {
   
    data(){
        return{
     
        }
    },
     components:{
        AsyncUser,
        LoadingComponent,
          ErrorComponent,
    }
    
}
</script>

<style>

</style>