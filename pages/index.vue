<template lang="">
  <div>
    <h1> Hello World </h1>
    <v-select v-model="selected" :options="options" placeholder="Select Category"></v-select>
  </div>
</template>
<script>
export default {
  data() {
    return {
      selected: '',
      options: [
        'foo',
        'bar',
        'baz'
      ]
    }
  }
}
</script>
<style lang="">
  
</style>