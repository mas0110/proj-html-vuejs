<script>

export default{
    name:"SectionPlayer",
    components:{
    }
}
</script>

<template>
<div class="container p-3">
    <div class="main-video">
        <iframe width="650" height="415" src="https://www.youtube.com/embed/kvqSDezN1S4?si=_VpJxUp96HghpKtv" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen>
        </iframe>
    </div>
    <div class="list-video">
        <div>
        <iframe width="300" height="200" src="https://www.youtube.com/embed/kvqSDezN1S4?si=_VpJxUp96HghpKtv" title="YouTube video player" frameborder="0" 
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        <h5>Rent a girlfriend season 2 official trailer</h5>
        </div>
        <div>
        <iframe width="300" height="200" src="https://www.youtube.com/embed/Gxt_FcBg2wE?si=12Y25vqH8vJ4O5GR" title="YouTube video player" frameborder="0" 
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        <h5>Overlord Season 4 - official trailer 3</h5>
        </div>
        <div>
        <iframe width="300" height="200" src="https://www.youtube.com/embed/4uSZTfsayQQ?si=iXkzp1MfQgqRSHux" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        <h5>uncle from another world - official trailer 2</h5>
        </div>
        <div>
        <iframe width="300" height="200" src="https://www.youtube.com/embed/HIjapMCjEBU?si=DHFOLi6Hj07CZLt0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        <h5>prima doll - official trailer</h5>
        </div>
        <div>
        <iframe width="300" height="200" src="https://www.youtube.com/embed/F1J3B3tCoV8?si=ilLcf18BaonTmbAG" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        <h5>shoot!goal to the future - official trailer </h5>
        </div>

    </div>
</div>
</template>

<style scoped lang="scss">
.container{
display: grid;
  grid-template-columns: 2fr 1fr;
}
.list-video{
overflow-y: scroll;
}

</style>
