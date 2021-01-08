<template lang="">
    <div>
        <div class="card bg-light mb-3" style="max-width: 18rem;">
            <div class="card-header"> Post : {{ post.id }}</div>
            <div class="card-body">
                <h5 class="card-title">{{ post.title }}</h5>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    props: {
        post: Object
    }
}
</script>
<style lang="">
    
</style>