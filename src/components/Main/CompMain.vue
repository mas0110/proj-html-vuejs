<script>
import SectionSlider from './SectionSlider.vue'
import SectionGrid from './SectionGrid.vue'
import SectionCategory from './SectionCategory.vue'
import SectionBanner from './SectionBanner.vue'
import SectionCarousel from './SectionCarousel.vue'
import SectionPlayer from './SectionPlayer.vue'
import SectionBox from './SectionBox.vue'


import { store } from '../../store'

export default {
    name: "CompMain",
    components: {
        SectionSlider,
        SectionGrid,
        SectionCategory,
        SectionBanner,
        SectionCarousel,
        SectionPlayer,
        SectionBox,
    },
    data() {
        return {
            store
        }
    },
    mounted(){
        // funzioni per slider quattro immagini

        let scrollContainer = this.$refs.scrollContainer;
        let backBtn = this.$refs.prev-img;
        let nextBtn = this.$refs.next-img;
    
        scrollContainer.addEventListener("wheel", (evt) => {
          evt.preventDefault();
          scrollContainer.scrollLeft += evt.deltaY;
          scrollContainer.style.scrollBehavior = "auto";
        });
    
        nextBtn.addEventListener("click", () => {
          scrollContainer.style.scrollBehavior = "smooth";
          scrollContainer.scrollLeft += 1100;
        });
    
        backBtn.addEventListener("click", () => {
          scrollContainer.style.scrollBehavior = "smooth";
          scrollContainer.scrollLeft -= 1100;
        });



        // funzioni per carosello a 3 immagini

        let carouselContainer = this.$refs.carouselContainer;
        let backImg = this.$refs.prev-btn;
        let nextImg = this.$refs.next-btn;

        carouselContainer.addEventListener("wheel", (ent) => {
          ent.preventDefault();
          carouselContainer.scrollLeft += evt.deltaY;
          carouselContainer.style.scrollBehavior = "auto";
        });
        nextImg.addEventListener("click", () => {
          carouselContainer.style.scrollBehavior = "smooth";
          carouselContainer.scrollLeft += 1150;
         });
        backImg.addEventListener("click", () => {
          carouselContainer.style.scrollBehavior = "smooth";
          carouselContainer.scrollLeft -= 1150;
        });
    },
    methods: {
    // slider 
    scrollNext() {
      let scrollContainer = this.$refs.scrollContainer;
      scrollContainer.style.scrollBehavior = "smooth";
      scrollContainer.scrollLeft += 1100;
    },
    scrollBack() {
      let scrollContainer = this.$refs.scrollContainer;
      scrollContainer.style.scrollBehavior = "smooth";
      scrollContainer.scrollLeft -= 1100;
    },

    // carousel
    playNext() {
      let carouselContainer = this.$refs.carouselContainer;
      carouselContainer.style.scrollBehavior = "smooth";
      carouselContainer.scrollLeft += 1150;
    },
    playBack() {
      let carouselContainer = this.$refs.carouselContainer;
      carouselContainer.style.scrollBehavior = "smooth";
      carouselContainer.scrollLeft -= 1150;
    }
  }
}
</script>

<template>
<main>
    <div class="thumbs">
    <button id="prev-img" ref="backBtn" @click="scrollBack">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - 
    https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l192 192c12.5 12.5 32.8 
    12.5 45.3 0s12.5-32.8 0-45.3L77.3 256 246.6 86.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-192 192z"/></svg>
    </button>
    <div class="row" ref="scrollContainer">
        <SectionSlider 
        v-for="(element, index) in store.content"
        :key="index"
        :propsImg= "element.img"
        :propsimgSmall= "element.imgSmall"
        :propsCategory1= "element.category1"
        :propsCategory2= "element.category2"
        :propsCategory3= "element.category3"
        :propsTitle= "element.title"
        :propsData="element.data"
        />
    </div> 
    <button id="next-img" ref="nextBtn" @click="scrollNext">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://    fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3     0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/></svg>
    </button>
    </div>


    <SectionGrid />
    <SectionCategory/>
    <SectionBanner/>


    <div class="container">
        <div class="d-flex justify-content-between">
            <h3>FEATURED POSTS</h3>
            <div>
                <button id="prev-btn" ref="backImg" @click="playBack">
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License -
                https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M9.4 233.4c-12.5 12.5-12.5 32.8 0 45.3l192 192c12.5 12.5 32.8 
                12.5 45.3 0s12.5-32.8 0-45.3L77.3 256 246.6 86.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0l-192 192z"/></svg>
                </button>
                <button id="next-btn" ref="nextImg" @click="playNext">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - 
                    https://
                    fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 
                    0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/></svg>
                </button>
            </div>
        </div>
        <div class="row riga" ref="carouselContainer">
            <SectionCarousel
             v-for="(element, index) in store.content"
             :key="index"
             :propsImg= "element.img"
             :propsimgSmall= "element.imgSmall"
             :propsCategory1= "element.category1"
             :propsCategory2= "element.category2"
             :propsCategory3= "element.category3"
             :propsTitle= "element.title"
             :propsData="element.data"/>
        </div>
    </div>
    <SectionPlayer/>
    <SectionBox/>
</main>
    
</template>

<style scoped lang="scss">
main{
padding-top: 160px;}
.container{
margin: 0 auto;
width: 80%;}
.row{
flex-wrap: nowrap;
position: relative;
overflow-x: scroll;
}
.row::-webkit-scrollbar{
display: none;
}

#prev-img, #next-img{
background-color: white;
border: 0;
height: 30px;
width: 30px;
border-radius: 50%;
position: absolute;
top: 45%;
transform: translate(-50%);
svg{
fill:red;
}
}

#prev-img{
left: 35px;
z-index: 1;
}

#next-img{
right: 15px;}

#prev-btn, #next-btn{
background-color: white;
border: 0;
height: 30px;
width: 30px;
border-radius: 50%;
background-color: black;
margin-left: 10px;
svg{
fill:white;
}
}

#prev-img:hover, #next-img:hover,
#prev-btn:hover, #next-btn:hover{
background-color: red;
svg{
fill:white}
}
</style>
