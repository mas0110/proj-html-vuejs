<script>

export default{
    name:"SectionPlayer",
    components:{
    },
    data() {
    return{
    mainVideoSrc: 'https://www.youtube.com/embed/kvqSDezN1S4?si=_VpJxUp96HghpKtv',
    videos: [
      {
        id: 'kvqSDezN1S4',
        title: 'Overlord Season 4 - official trailer 3',
        thumbnail: 'src/assets/img/default.webp',
        number: 1,
      },
      {
        id: 'ErhbPRW6ehc',
        title: 'Rent a girlfriend season 2 official trailer',
        thumbnail: 'src/assets/img/Rentagirlfriend.jpeg',
        number: 2,
      },
      {
        id: '3YVeAJ-n4ho',
        title: 'uncle from another world - official trailer 2',
        thumbnail: 'src/assets/img/uncleromanotherworld .jpeg',
        number: 3,
      },
      {
        id: '5JoibuETRCI',
        title: 'prima doll - official trailer',
        thumbnail: 'src/assets/img/primadoll .jpeg',
        number: 4,
      },
      {
        id: '1T7BFGACOU0',
        title: 'shoot!goal to the future - official trailer',
        thumbnail: 'src/assets/img/shoot!goal .jpeg',
        number: 5,
      },
    ],
     mainVideoId: 'kvqSDezN1S4',
    }

  },
  methods: {
    changeMainVideo(videoid) {
      this.mainVideoSrc = `https://www.youtube.com/embed/${videoid}?si=_VpJxUp96HghpKtv`;
      this.mainVideoId = videoid;
    },
  },
  mounted(){

    function changeMainVideo(videoid) {
      
      const mainVideo = document.querySelector('.main-video iframe');
    
     
      mainVideo.src = `https://www.youtube.com/embed/${videoid}?si=_VpJxUp96HghpKtv`;
    
      
      const activeVideo = document.querySelector('.list-video .vid .active');
      activeVideo.classList.remove('active');
    
      const newActiveVideo = document.querySelector(`.list-video .vid[data-id="${videoid}"]`);
      newActiveVideo.classList.add('active');
    }

    document.querySelectorAll('.list-video .vid').forEach(video => {
      video.addEventListener('click', () => {
        const videoid = video.getAttribute('data-id');
        changeMainVideo(videoid);
      });
    });
  },
}
</script>

<template>
<div class="container p-3 mt-5">
    <div class="main-video">
        <iframe width="750" height="450" v-bind:src="mainVideoSrc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen>
        </iframe>
    </div>
    <div class="list-video">
        <div class="banner">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512"><!--!Font Awesome Free 6.5.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2024 Fonticons, Inc.--><path d="M73 39c-14.8-9.1-33.4-9.4-48.5-.9S0 62.6 0 80V432c0 17.4 9.4 33.4 24.5 41.9s33.7 8.1 48.5-.9L361 297c14.3-8.7 23-24.2 23-41s-8.7-32.2-23-41L73 39z"/></svg>
            <span>
            video playlist 1/5
            </span>
        </div>
        <div v-for="video in videos" :key="video.id" class="vid" :class="{ active: video.id === mainVideoSrc }">
             <span>{{ video.number }}</span>
            <figure>
                <img v-bind:src="video.thumbnail">
            </figure>
            <h5>{{ video.title }}</h5>
            <hr>
        </div>
    </div>
</div>
</template>

<style scoped lang="scss">
.container{
display: flex;
margin-top: 30px;
}
.list-video{
overflow-y: scroll;
height: 450px;
background-color: #F3F3F3;
// padding: 20px;
// position: relative;
// padding-top: 80px;
}
.vid{
display: flex;
gap: 10px;
margin-block: 20px;
display: flex;
align-items: center;
    figure{
    margin: 0;
        img{
        border-radius:  10px;
        width: 100px;
        height: 70px;
        }
    }
    h5{
    opacity: 60%;
    }
    span{
    height: 30px;
    aspect-ratio: 1;
    text-align: center;
    border-radius: 50%;
    }
}
.banner{
background-color: #333333 ;
color: white;
height: 30px;
padding: 40px;
position: sticky;
top: 0;
right: 0;
left: 0;
display: flex;
align-items: center;
justify-content: left;
gap: 10px;
   svg{
   fill: white;
   }
}
.active span{
background-color: red;
}

</style>
