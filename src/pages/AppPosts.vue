<template>
  <div class="container">
      <ul class="list-group" v-for="(post, key) in posts" :key="key">
    
        <li class="list-group-item"><h3>{{ post.title }}</h3></li>
       
      </ul>
  </div>
</template>

<script>
import {postService} from '../service/PostService'
export default {
    data(){
        return{
            posts: []
        }
    },
 
}
</script>