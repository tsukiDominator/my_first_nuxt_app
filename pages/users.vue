<template>
    <div>
        <h1>这是父级</h1>
        <input type="text" v-model="userID">
        <button v-on:click="onLoadUser">用户详情</button>
        <nuxt-child></nuxt-child>
    </div>
</template>

<script>
export default {
    data(){
        return{
            userID:""
        }
    },
    methods:{
        onLoadUser(){
            this.$router.push('/users/'+this.userID)
        }
    },
    //layout:'users'
}
</script>
