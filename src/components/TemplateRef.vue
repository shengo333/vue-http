<template>
    <div>
        <input type="text" ref="inputRef">
        <PostList ref="PostListRef" />
    </div>
</template>

<script>

import PostList from './PostList.vue'
export default {
    name: 'TemplateRef',
    components:{PostList},
    mounted(){
        console.log(this.$refs.PostListRef)
        this.$refs.inputRef.focus()
    }
}
</script>

<style>

</style>