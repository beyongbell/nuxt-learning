<template lang="">
    <div>
        <h1> Users id : {{ $route.params.id }} </h1>
    </div>
</template>
<script>
export default {
    validate({params}) {
        return /^\d+$/.test(params.id)
    }
}
</script>
<style lang="">
    
</style>