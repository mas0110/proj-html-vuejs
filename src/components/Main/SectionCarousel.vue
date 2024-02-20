<script>

export default{
    name:"SectionCarousel",
    components:{
    }
}
</script>

<template>
<div class="container">
 <div class="cont col-3 d-flex justify-content-center">
      <div class="card bg-light text-center" style="width: 20rem;">
           <img :src="propsImg" alt="...">
           <div class="card-body">
               <h5 class="card-title">{{propsTitle}}</h5>
               <span class="opacity-50">{{propsData}}</span>
               <div class="category">
                  <a href="#">{{propsCategory1}}</a>
                  <a href="#">{{ propsCategory2 }}</a>
                  <a href="#">{{ propsCategory3 }}</a>
               </div>
           </div>
      </div>
 </div>
</div>
</template>

<style scoped lang="scss">
    .container{
        width: 80%;
        margin: 0 auto;
    }
</style>
