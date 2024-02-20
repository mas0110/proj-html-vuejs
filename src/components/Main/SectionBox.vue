<script>

export default{
    name:"SectionBox",
    components:{
    }
}
</script>

<template>
<div class="box-container">
    <div class="box">
        <figure>
            <img src="../../assets/img/anime-fashion.webp" alt="">
        </figure>
        <h4>fashion</h4>
    </div>
     <div class="box">
     <figure>
         <img src="../../assets/img/success-story.webp" alt="">
     </figure>
     <h4>culture</h4>
 </div> <div class="box">
     <figure>
         <img src="../../assets/img/healthy-foods.webp" alt="">
     </figure>
     <h4>food</h4>
 </div> <div class="box">
     <figure>
         <img src="../../assets/img/visit-france.webp" alt="">
     </figure>
     <h4>lifestyle</h4>
 </div> <div class="box">
     <figure>
         <img src="../../assets/img/travel-alone.webp" alt="">
     </figure>
     <h4>stories</h4>
 </div> <div class="box">
     <figure>
         <img src="../../assets/img/best-places.webp" alt="">
     </figure>
     <h4>travel</h4>
 </div>
</div>
</template>

<style scoped lang="scss">
figure img{
height: 150px;
aspect-ratio: 3/2;
border-radius: 5px;
filter: brightness(0.6);
}

figure img:hover{
filter: brightness(1);
}
.box{
position: relative;
width: calc(100% / 6);
}
.box h4{
position: absolute;
top: 50%;
left: 50%;
transform: translate(-50%, -50%);
color: white;
text-transform: uppercase;
}
.box-container{
display: flex;
padding-left: 20px;
margin-top: 50px;
}
</style>
