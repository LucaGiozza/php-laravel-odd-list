<template>
  <div class="container">
   <div class="row">
    <div class="col-sm-6">
      <div class="card">
        <div class="card-body">
          <h5 class="card-title">Special title treatment</h5>
          <p class="card-text">With supporting text below as a natural lead-in to additional content.</p>
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
            callApi:'http://localhost8000/api/posts'
        }
    },

    created(){
        this.stampaNome();
        console.log(this.callApi);
    },
    methods:{
        stampaNome(){
            console.log('pippo')
        }
    }

  
}
</script>

<style lang="scss" scoped>

</style>