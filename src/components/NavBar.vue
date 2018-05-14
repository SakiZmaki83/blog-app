<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-secondary">
      <router-link class="navbar-brand" to="/">Blog</router-link>
     
    
        <div class="navbar-nav">
          <router-link class="nav-item nav-link" to="/posts">Posts</router-link>
          <router-link class="nav-item nav-link" to="/add">Add post</router-link>
        
      </div>
    </nav>
  </div>
</template>

<script>
export default {
}
</script>