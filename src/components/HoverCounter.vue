<template>
  <div>
      <button @mouseover="incrementCount">Hovered {{count}} </button>
  </div>
</template>

<script>

import counterMixin from '../mixins/counter.js'

export default {
    name: 'HoverCounter',
    mixins:[counterMixin]
}
</script>

<style>

</style>