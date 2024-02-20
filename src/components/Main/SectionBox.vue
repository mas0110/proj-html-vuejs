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
            <span>4 post</span>
        </figure>
        <h4>fashion</h4>
    </div>
     <div class="box">
     <figure>
         <img src="../../assets/img/success-story.webp" alt="">
         <span>4 post</span>
     </figure>
     <h4>culture</h4>
 </div> <div class="box">
     <figure>
         <img src="../../assets/img/healthy-foods.webp" alt="">
         <span>4 post</span>
     </figure>
     <h4>food</h4>
 </div> <div class="box">
     <figure>
         <img src="../../assets/img/visit-france.webp" alt="">
         <span>4 post</span>
     </figure>
     <h4>lifestyle</h4>
 </div> <div class="box">
     <figure>
         <img src="../../assets/img/travel-alone.webp" alt="">
         <span>4 post</span>
     </figure>
     <h4>stories</h4>
 </div> <div class="box">
     <figure>
         <img src="../../assets/img/best-places.webp" alt="">
         <span>4 post</span>
     </figure>
     <h4>travel</h4>
 </div>
</div>
</template>

<style scoped lang="scss">
figure img{
height: 200px;
aspect-ratio: 1;
border-radius: 5px;
 object-fit: cover;
}

figure::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 200px;
  height: 200px;
  background-color: rgba(217, 3, 3, 0); 
  transition: background-color 0.3s ease;
}
figure:hover::before {
  background-color: rgba(217, 3, 3, 0.5); 
}
figure:hover span{
display: block;
}

.box{
position: relative;
width: calc(100% / 6);
height: 200px;
aspect-ratio: 1;
 span{
 display: none;
 position: absolute;
 top: 70%;
 left: 50%;
 transform: translate(-50%, -50%);
 color: white;
 }
}
.box h4{
position: absolute;
top: 50%;
left: 50%;
transform: translate(-50%, -50%);
color: white;
text-transform: uppercase;
padding: 30px;
}
.box-container{
display: flex;
padding-left: 20px;
margin-top: 50px;
padding-bottom: 20px;
}
</style>
