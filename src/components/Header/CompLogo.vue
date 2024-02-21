<script>

export default{
    name:"CompLogo",
    components:{
    }
}
</script>

<template>
<div class="container py-2">
    <div>
        <figure class="d-flex justify-content-around">
            <img src="../../assets/img/anime-logo-300x89.webp" alt="white-logo">
            <img src="../../assets/img/page-banner-1-768x71.webp" alt="page-banner">
        </figure>
    </div>
</div>
</template>

<style scoped>
    .container{
        width: 80%;
        margin: 0 auto;
    }
    img:first-child{
        width: 200px;
    }
    img:last-child{
        width: 550px;
        border-radius: 5px;
    }
</style>
