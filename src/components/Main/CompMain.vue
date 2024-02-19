<script>
import SectionSlider from './SectionSlider.vue'
import SectionGrid from './SectionGrid.vue'
import { store } from '../../store'

export default {
    name: "CompMain",
    components: {
        SectionSlider,
        SectionGrid
    },
    data() {
        return {
            store
        }
    },
}
</script>

<template>
    <div class="row">
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
    <SectionGrid />
</template>

<style></style>
