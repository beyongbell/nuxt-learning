<template lang="">
    <div>
        <h2> Make API Request - the Vue Way </h2>
        <div class="container row">
            <Card v-for="(post, index) in posts" :key="post.id" :post="post" class="ml-auto mr-auto" />
        </div>
    </div>
</template>
<script>
import axios from 'axios'
import Card from '@/components/Card'
export default {
    components: {
        Card
    },
    data() {
        return {
            posts: ''
        }
    },
    async asyncData({store}) {
        // let response = await axios.get('https://jsonplaceholder.typicode.com/todos')
        // return { posts : response.data }
        let {data} = await axios.get('https://jsonplaceholder.typicode.com/posts')
        store.dispatch('setPosts', data)
    },
    head: {
        title: 'List of Post'
    }
}
</script>
<style lang="">
    
</style>