<template>
<div>
<app-header></app-header>
<router-view></router-view>
</div>
</template>

<script>
import addblog from './components/addBlog.vue'
import showblog from './components/showBlogs.vue'
import listblog from './components/listBlogs.vue'
import header from './components/header.vue'
import singleblog from './components/singleBlog.vue'
export default {
  components: {

    'add-blog': addblog,
    'show-blog': showblog,
    'list-blog': listblog,
    'app-header': header,
    'single-blog': singleblog
  },
  data() {
      return {


    }
    },

  methods: {




  }
  }


</script>

<style scoped>


</style>
