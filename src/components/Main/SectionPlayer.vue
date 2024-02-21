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
        <iframe width="750" height="450" src="https://www.youtube.com/embed/kvqSDezN1S4?si=_VpJxUp96HghpKtv" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen>
        </iframe>
    </div>
    <div class="list-video">
        <div class="banner">
            <span>
            video playlist 1/5
            </span>
        </div>
        <hr>
        <div class="vid">
            <figure>
                <img src="../../assets/img/default.webp" alt="">
            </figure>
            <h5>Overlord Season 4 - official trailer 3</h5>
        </div>
        <hr>
        <div class="vid">
            <figure>
                <img src="../../assets/img/default.webp" alt="">
            </figure>
             <h5>Rent a girlfriend season 2 official trailer</h5>
        </div>
        <hr>
        <div class="vid">
            <figure>
                <img src="../../assets/img/default.webp" alt="">
            </figure>
            <h5>uncle from another world - official trailer 2</h5>
        </div>
        <hr>
        <div class="vid">
            <figure>
                <img src="../../assets/img/default.webp" alt="">
            </figure>
            <h5>prima doll - official trailer</h5>
        </div>
        <hr>
        <div class="vid">
            <figure>
                <img src="../../assets/img/default.webp" alt="">
            </figure>
            <h5>shoot!goal to the future - official trailer </h5>
        </div>

    </div>
</div>
</template>

<style scoped lang="scss">
.container{
display: flex;
}
.list-video{
overflow-y: scroll;
height: 450px;
background-color: #F3F3F3;
padding: 20px;
position: relative;
padding-top: 55px;
}
.vid{
display: flex;
gap: 10px;
    figure{
    margin: 0;
        img{
        border-radius:  10px;
        height: 60px;
        }
    }
    h5{
    opacity: 60%;
    }
}
.banner{
background-color:#333333 ;
color: white;
height: 30px;
padding: 40px;
position: absolute;
top: 0;
right: 0;
left: 0;

}

</style>
