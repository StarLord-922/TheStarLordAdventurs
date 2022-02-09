<template>
    <h3>This is my list</h3>
            <div v-if="error">{{error}}</div>
            <User v-else v-for="user in users.data" key="user.id" :user="user" />
       
        
</template>

<script>
import axios from "axios"
import User from "./User.vue"
import {ref} from "vue"
export default {
    name:"Users",

    async setup() {
        const error=ref(null)
        const users=ref(null)
        try{
            const userResponse= await fetch("https://reqres.in/api/users?delay=3")
            users.value= await userResponse.json()
        }
        catch(err){
            console.log(err)
            error.value=err
        }
        return {users,error}
    
    },
    data(){
        return{
            users:null
        }
    },
    components:{
        User
    },

}
</script>


<style>

</style>