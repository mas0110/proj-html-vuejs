<script>

export default {
    name: "SectionCategory",
    components: {
    },
    props: [
        'propsImg',
        'propsimgSmall',
        'propsCategory1',
        'propsCategory2',
        'propsCategory3',
        'propsTitle',
        'propsData'
    ]
}
</script>

<template>
<div class="container mt-5" id="lifestyle">
    <div class="d-flex justify-content-between my-3">
        <h3>LIFESTYLE & STORIES</h3>
        <div>
            <button class="btn btn-secondary">ALL</button>
            <button class="btn btn-secondary mx-3">LIFESTYLE</button>
            <button class="btn btn-secondary">STORIES</button>
        </div>
    </div>
    <div class="d-flex gap-3 justify-content-around">
        <div>
            <div class="main bg-light text-center" style="width: 30rem;">
                <img src="../../assets/img/success-story.webp" alt="">
                <div class="cardBody">
                     <div class="text d-flex flex-column text-start">
                        <span class="text-light">december 26, 2022</span>
                        <h5 class="card-title text-light">the best success stories</h5>
                    </div>
                    <div class="category">
                        <a href="#">Culture</a>
                    </div>
                </div>
            </div>
        </div>
        <div class="side">
            <div class="cont col-3 d-flex justify-content-between">
                <div class="d-flex gap-3" style="width: 20rem;">
                    <img src="../../assets/img/travel-alone-300x200.webp" alt="...">
                    <div class="card-body">
                        <span class="opacity-50">december 26, 2022</span>
                        <h5 class="card-title">travelling alone is awesome</h5>
                        <a class="tag" href="#">stories</a>
                    </div>
                </div>
            </div>
            <hr>
            <div class="cont col-3 d-flex justify-content-between my-2">
                <div class="d-flex gap-3" style="width: 20rem;">
                    <img src="../../assets/img/best-places.webp" alt="...">
                    <div class="card-body">
                        <span class="opacity-50">decembre 25, 2022</span>
                        <h5 class="card-title">places for a road trip</h5>
                        <a class="tag" href="#">lifestyle</a>
                    </div>
                </div>
            </div>
            <hr>
            <div class="cont col-3 d-flex justify-content-between">
                <div class="d-flex gap-3" style="width: 20rem;">
                    <img src="../../assets/img/music-love.webp" alt="...">
                    <div class="card-body">
                        <span class="opacity-50">decembre 25, 2022</span>
                        <h5 class="card-title">music the love of my life </h5>
                        <a class="tag" href="#">culture</a>
                    </div>
                </div>
            </div>

        </div>
    </div>
</div>
</template>

<style scoped lang=scss>
.container{
margin: 0 auto;
width: 80%;}
.side{
width: 500px;
background-color: white;
margin-left: 220px;
    img{
    height: 150px;
    filter: brightness(0.6);
    }
    img:hover{
    filter: brightness(1);
    }
}

a{
    background-color: white;
    text-decoration: none;
    color: black;
    margin: 10px;
    padding: 3px;
    border-radius: 5px;
}

img{
border-radius: 5px;
}

.main img{
    width: 700px;
    height: 520px;
    filter: brightness(0.6);
    
}
.main img:hover{
    filter: brightness(1);
}

.main{
    position: relative;
}
.category {
    position: absolute;
    top: 10px;
    left: 10px;
}
.text{
position: absolute;
bottom: 10px;
left: 10px;
}
.cont{
position: relative;
   a{
   position: absolute;
   top: 10px;
   left: 10px;
   }
}

</style>