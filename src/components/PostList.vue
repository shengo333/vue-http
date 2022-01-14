<template>
  <!-- <button @click="getPosts">Load Posts</button> -->
  <h3 v-if="errorMSG">{{errorMSG}}</h3>
  <div v-for="post in posts" :key="post.id">
      <h2>{{post.id}} {{post.title}}</h2>
      <p>{{post.body}}</p>
  </div>
</template>

<script>

import axios from 'axios'

export default {
    name: 'PostList',
    created(){
        console.log('created')
        this.getPosts()
    },
    data(){
        return {
            posts:[],
            errorMSG:'',
        }
    },
    methods:{
        getPosts(){
            axios.get('https://jsonplaceholder.typicode.com/posts')
            .then((response)=>{
                console.log(response.data)
                this.posts = response.data
            })
            .catch((error)=>{
                error = console.log(error.data)
                this.errorMSG = 'error retriving data'
            })
        }
    }
}
</script>

<style scoped>

</style>