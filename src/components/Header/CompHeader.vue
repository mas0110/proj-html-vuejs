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
    <header>
       <CompUpdates/>
       <CompLogo/>
       <CompItem/>
    </header>
</template>

<style>
svg{
    height: 20px;
}
header{
position: fixed;
top: 0;
left: 0;
right: 0;
z-index: 3;
background-color: white;
}
</style>
