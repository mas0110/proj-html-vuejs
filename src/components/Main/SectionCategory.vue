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
<div class="container mt-5">
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
                     <div class="text d-flex flex-column text-center">
                        <h5 class="card-title">ciao</h5>
                        <span class="opacity-50">ciao</span>
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
                        <span class="opacity-50">span</span>
                        <h5 class="card-title">h5</h5>
                        <a class="tag" href="#">ciao</a>
                    </div>
                </div>
            </div>
            <hr>
            <div class="cont col-3 d-flex justify-content-between my-2">
                <div class="d-flex gap-3" style="width: 20rem;">
                    <img src="../../assets/img/travel-alone-300x200.webp" alt="...">
                    <div class="card-body">
                        <span class="opacity-50">span</span>
                        <h5 class="card-title">h5</h5>
                        <a class="tag" href="#">ciao</a>
                    </div>
                </div>
            </div>
            <hr>
            <div class="cont col-3 d-flex justify-content-between">
                <div class="d-flex gap-3" style="width: 20rem;">
                    <img src="../../assets/img/travel-alone-300x200.webp" alt="...">
                    <div class="card-body">
                        <span class="opacity-50">span</span>
                        <h5 class="card-title">h5</h5>
                        <a class="tag" href="#">ciao</a>
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
    width: 200px;
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

</style>