<template>
<div id="single-blog">
<h1>{{blog.title}}</h1>
<article>
{{blog.content}}


</article>
<p>Author: {{blog.author}}</p>
<ul v-for="category in blog.categories">
<li>
{{category}}
</li>
</ul>
</div>

</template>

<script>

export default {
  components: {

  },
  data() {
      return {
        id: this.$route.params.id,
        blog: {}

    }
    },

  methods: {




  },
  created() {
      this.$http.get('https://vuetrail-efb54-default-rtdb.firebaseio.com/posts/'+this.id+'.json').then(function(data){
      return data.json();
     }).then(function(data){
      this.blog = data;
    });






  }
  }


</script>

<style scoped>
#single-blog{
max-width: 960px;
margin: 0 auto;


}

</style>
