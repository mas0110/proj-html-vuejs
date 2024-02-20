<script>
import SectionSlider from './SectionSlider.vue'
import SectionGrid from './SectionGrid.vue'
import SectionCategory from './SectionCategory.vue'
import SectionBanner from './SectionBanner.vue'
import SectionCarousel from './SectionCarousel.vue'


import { store } from '../../store'

export default {
    name: "CompMain",
    components: {
        SectionSlider,
        SectionGrid,
        SectionCategory,
        SectionBanner,
        SectionCarousel,
    },
    data() {
        return {
            store
        }
    },
    mounted(){
        let scrollContainer = this.$refs.scrollContainer;
        let backBtn = this.$refs.prev-img;
        let nextBtn = this.$refs.next-img;
    
        scrollContainer.addEventListener("wheel", (evt) => {
          evt.preventDefault();
          scrollContainer.scrollLeft += evt.deltaY;
          scrollContainer.style.scrollBehavior = "auto";
        });
    
        nextBtn.addEventListener("click", () => {
        //   scrollContainer.style.scrollBehavior = "smooth";
          scrollContainer.scrollLeft += 1100;
          console.log("ciao")
        });
    
        backBtn.addEventListener("click", () => {
        //   scrollContainer.style.scrollBehavior = "smooth";
          scrollContainer.scrollLeft -= 1100;
           console.log("ciao")
        });
    },
    methods: {
    scrollNext() {
      let scrollContainer = this.$refs.scrollContainer;
    //   scrollContainer.style.scrollBehavior = "smooth";
      scrollContainer.scrollLeft += 1100;
    },
    scrollBack() {
      let scrollContainer = this.$refs.scrollContainer;
    //   scrollContainer.style.scrollBehavior = "smooth";
      scrollContainer.scrollLeft -= 1100;
    }
  }
};
</script>

<template>
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
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M310.6 233.4c12.5 12.5 12.5 32.8 0 45.3l-192 192c-12.5 12.5-32.8 12.5-45.3 0s-12.5-32.8 0-45.3L242.7 256 73.4 86.6c-12.5-12.5-12.5-32.8 0-45.3s32.8-12.5 45.3 0l192 192z"/></svg>
</button>
</div>
    <SectionGrid />
    <SectionCategory/>
    <SectionBanner/>
    <SectionCarousel/>
</template>

<style scoped lang="scss">
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
top: 50%;
transform: translate(-50%);
svg{
fill:red;
}
}

#prev-img{
left: 20px;
z-index: 1;
}

#next-img{
right: 20px;}
</style>
