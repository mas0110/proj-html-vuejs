<script>
 import CompUpdates from './CompUpdates.vue'
 import CompLogo from './CompLogo.vue'

export default{
    name:"CompHeader",
    components:{
        CompUpdates,
        CompLogo
    }
}
</script>

<template>
   <CompUpdates/>
   <CompLogo/>
</template>

<style>
ul li svg{
    height: 20px;
}
</style>
