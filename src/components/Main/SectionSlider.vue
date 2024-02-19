
<script>

export default{
    name:"SectionSlider",
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
</template>

<style scoped lang="scss">
.cont{
    background-color:#F3F3F3 ;
    div img{
        min-width: 320px;
        aspect-ratio: 4/3;
    }
    .card{
        height: 360px;
        margin-top: 20px;
        position: relative;
    }
    .category{
        position: absolute;
        top: 10px;
        left: 50%;
        transform: translate(-50%);
        a{
            background-color: white;
            text-decoration: none;
            color: black;
            margin: 10px;
            padding: 3px;
            border-radius: 5px;
        }

    }
}
</style>