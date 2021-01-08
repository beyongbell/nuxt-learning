<template lang="">
    <div>
        <h2> Make API Request - the Vue Way </h2>
        <div class="container">
            <h2 v-for="(post, index) in posts" :key="post.id">
                {{ post.title }}
            </h2>
        </div>
    </div>
</template>
<script>
import axios from 'axios'
export default {
    data() {
        return {
            posts: ''
        }
    },
    asyncData() {
        return axios.get('https://jsonplaceholder.typicode.com/todos')
        .then(response => {
           return { posts : response.data }
        })
    },
}

// export default {
//     data() {
//         return {
//             posts: []
//         }
//     },
//     mounted() {
//         axios.get('https://jsonplaceholder.typicode.com/todos')
//         .then(response => {
//             console.log(response.data)
//             this.posts = response.data
//         })
//         .catch(error => {
//             console.log(error)
//         })
//     }
// }
</script>
<style lang="">
    
</style>