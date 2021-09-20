<template>
  <div class="container">
      <p>Pagina corrente {{currentPage}} - ultima pagina sarà {{lastPage}}</p>
   <div class="row">
    <div class="col-sm-6" v-for="post in posts" :key="post.id">
      <div class="card mt-4">
        <div class="card-body">
          <h5 class="card-title">{{post.title}}</h5>
          <p class="card-text">{{post.content}}</p>
          <a href="#" class="btn btn-primary">Go somewhere</a>
       </div>
    </div>
  </div>

 </div>
</div>
</template>

<script>
export default {
    name: "Main",

    data(){
        return{
            callApi:'http://localhost:8000/api/posts',
            posts: [],
            currentPage: 1,
            lastPage: null
        }
    },

    created(){
        this.getPosts();
       
    },
    methods:{
        getPosts(){
           axios.get(this.callApi)
           .then(response => {
               
               this.posts = response.data.results.data;
               
               this.currentPage = response.data.results.current_page;
               this.lastPage = response.data.results.last_page;
           })
           .catch();
        }
    }

  
}
</script>

<style lang="scss" scoped>

</style>