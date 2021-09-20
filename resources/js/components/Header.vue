<template>
    <div>
     <nav class="navbar navbar-expand-lg navbar-light bg-light">
       <div class="container-fluid">
         <a class="navbar-brand" href="#">Boolpress</a>
         <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
           <span class="navbar-toggler-icon"></span>
         </button>
         <div class="collapse navbar-collapse" id="navbarNav">
           <ul class="navbar-nav">
             <li class="nav-item">

                 <router-link :to="{ name: 'home'}" class="nav-link active">

                     Home
                 </router-link>
                
             </li>
             <li class="nav-item">
                 <router-link :to="{ name: 'about'}" class="nav-link">
                     Chi siamo

                 </router-link>

               
             </li>
             <li class="nav-item">
                <a class="nav-link" href="#">Contatti</a>
             </li>
             
           </ul>
         </div>
       </div>
     </nav>
 </div>
</template>

<script>
export default {
    name: "Header"
     
}
</script>
<style lang="scss" scoped>

</style>