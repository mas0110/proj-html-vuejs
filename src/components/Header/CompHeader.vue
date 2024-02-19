<script>
 import CompUpdates from './CompUpdates.vue'
 import CompLogo from './CompLogo.vue'
 import CompItem from './CompItem.vue'

export default{
    name:"CompHeader",
    components:{
        CompUpdates,
        CompLogo,
        CompItem
    }
}
</script>

<template>
   <CompUpdates/>
   <CompLogo/>
   <CompItem/>
</template>

<style>
svg{
    height: 20px;
}
</style>
