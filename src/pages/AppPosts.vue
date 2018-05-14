<template>
    <div>

        <table class="table">
            <thead class="thead-dark">
            <tr>
                <th scope="col">Id</th>
                <th scope="col">Title</th>
                <th scope="col">Text</th>
                <th scope="col">CreatedAt</th>
            </tr>
            </thead>
            <tbody>

            <tr v-for="(post,key) in posts" :key='key'>
                <th scope="row">{{post.id}}</th>
                <td>{{ post.title}}</td>
                <td>{{ post.text}}</td>
                <td>{{ post.createdAt}}</td>
                <td><router-link class="btn btn-primary" :to="{name: 'single-post', params: {id: post.id}}">View Post</router-link></td>
              
            </tr>
            </tbody>
        </table>

    </div>
</template>


<script>
    import {postServ} from "../services/postServices";
    export default {
        name: "AppPosts",
        created() {
            this.getAll()
        },
        data() {
            return {
                posts: []
            }
        },
        
        methods: {
            getAll() {
                postServ.getAll()
                    .then((response) => {
                        
                        this.posts = response.data
                    });
            },
           
        }
    }
</script>

<style scoped>
</style>
