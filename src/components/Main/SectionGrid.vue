<script>
export default {
    name: "SectionGrid",
    components: {

    }
}

</script>

<template>
    <div class="container d-flex justify-content-center mt-5 gap-2">
        <div>
            <div class="side card bg-light text-center" 
            style="width: 20rem; background-image: url(src/assets/img/anime-fashion.webp); background-size:cover;">

                <div class="card-body">
                    <div class="text d-flex flex-column text-center">
                        <h5 class="card-title">ciao</h5>
                        <span class="opacity-50">ciao</span>
                    </div>
                    <div class="category">
                        <a href="#">ciao</a>
                        <a href="#">ciao</a>
                        <a href="#">ciao</a>
                    </div>
                </div>
            </div>
            <div class="side card bg-light text-center" style="width: 20rem; background-image: url(src/assets/img/travel-alone-300x200.webp); background-size:cover;">
                <div class="card-body">
                    <div class="text d-flex flex-column text-center">
                        <h5 class="card-title">ciao</h5>
                        <span class="opacity-50">ciao</span>
                    </div>
                    <div class="category">
                        <a href="#">ciao</a>
                        <a href="#">ciao</a>
                        <a href="#">ciao</a>
                    </div>
                </div>
            </div>
        </div>


        <div>
            <div class="main card bg-light text-center" style="width: 30rem; background-image: url(src/assets/img/best-places.webp); background-size:cover;">
                <div class="card-body">
                    <div class="text d-flex flex-column text-center">
                        <h5 class="card-title">ciao</h5>
                        <span class="opacity-50">ciao</span>
                    </div>
                    <div class="category">
                        <a href="#">ciao</a>
                        <a href="#">ciao</a>
                        <a href="#">ciao</a>
                    </div>
                </div>
            </div>
        </div>


        <div>
            <div class="side card bg-light text-center" style="width: 20rem; background-image: url(src/assets/img/music-love.webp); 
            background-size:cover;">
                <div class="card-body">
                    <div class="text d-flex flex-column text-center">
                        <h5 class="card-title">ciao</h5>
                        <span class="opacity-50">ciao</span>
                    </div>
                    <div class="category">
                        <a href="#">ciao</a>
                        <a href="#">ciao</a>
                        <a href="#">ciao</a>
                    </div>
                </div>
            </div>
            <div class="side card bg-light text-center" style="width: 20rem; background-image: url(src/assets/img/visit-france.webp);
            background-size:cover;">
                <div class="card-body">
                    <div class="text d-flex flex-column text-center">
                        <h5 class="card-title">ciao</h5>
                        <span class="opacity-50">ciao</span>
                    </div>
                    <div class="category">
                        <a href="#">ciao</a>
                        <a href="#">ciao</a>
                        <a href="#">ciao</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
.card {
    position: relative;
    .text {
        position: absolute;
        bottom: 10px;
        right: 50%;
        transform: translate(-50%);
    }
}
.card:hover{
filter: brightness(0.7);
}

.category {
    position: absolute;
    top: 10px;
    left: 50%;
    transform: translate(-50%);

    a {
        background-color: white;
        text-decoration: none;
        color: black;
        margin: 10px;
        padding: 3px;
        border-radius: 5px;
    }
}

.side {
    height: 200px;
    margin-bottom: 10px;
}

.main {
    height: 400px;
    aspect-ratio: 4/3;
}
</style>
