<template>
  <div>
      <button @click="incrementCount">Clicked {{count}} </button>
  </div>
</template>

<script>

import counterMixin from '../mixins/counter.js'

export default {
    name: 'ClickCounter',
    data(){
        return{
            count: 100,
        }
    },    
    mixins:[counterMixin]

}
</script>

<style>

</style>