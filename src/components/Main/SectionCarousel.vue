<script>

export default{
    name:"SectionCarousel",
    components:{
    },
    props:[
    'propsImg',
    'propsimgSmall',
    'propsCategory1',
    'propsCategory2',
    'propsCategory3',
    'propsTitle',
    'propsData'
    ]
}
</script>

<template>
 <div class="cont col-4 d-flex justify-content-center m-0" id="stories">
      <div class="card bg-light text-center" style="width: 25rem;">
           <img :src="propsImg" alt="...">
           <div class="card-body mt-3">
               <h5 class="card-title">{{propsTitle}}</h5>
               <span class="opacity-50">{{propsData}}</span>
               <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum, omnis.</p>
               <button class="btn">Read More</button>
           </div>
      </div>
 </div>
</template>

<style scoped lang="scss">
.card{
height: 450px;
div button{
background-color: #BF1E2E;
color: white;
border-radius: 20px;
}
button:hover{
background-color:#4F514C ;
}
}
</style>
