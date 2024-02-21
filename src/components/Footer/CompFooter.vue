<script>
// import CompSinglecard from './CompSinglecard.vue'

export default{
    name:"CompFooter",
    components:{
        
}
}
</script>

<template>
   <div class="bg">
        <div class="list-container">
            <ul>
                 <h5>get started</h5>
                  <li>resources</li>
                  <li>tutorials</li>
                  <li>example</li>
                  <li>docs</li>
            </ul>
            <ul>
                 <h5>about</h5>
                  <li>stories</li>
                  <li>community</li>
                  <li>blog</li>
                  <li>brand assets</li>
            </ul>
            <ul>
                 <h5>features</h5>
                  <li>oveview</li>
                  <li>design</li>
                  <li>code</li>
                  <li>collaborate</li>
            </ul>
            <ul>
                 <h5>quick links</h5>
                  <li>stories</li>
                  <li>community</li>
                  <li>blog</li>
                  <li>brand assets</li>
            </ul>
            <div>
               <h5>subscribe to newsletter</h5>
               <div class="mb-3">
                 <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="Email">
                 <button class="btn btn-secondary mt-3 w-100">SUBSCRIBE</button>
               </div>
            </div>
        </div>
        <div class="line"></div>
        <div class="logo-container d-flex">
            <figure>
                <img src="../../assets/img/anime-whitelogo-300x89.png" alt="logo">
            </figure>
            <span> &#169; anime tech theme by hansanai dev</span>
        </div>

   </div>
</template>

<style scoped lang="scss">
.bg{
background-color:#BF1E2E ;
}
.list-container{
width: 80%;
margin: 0 auto;
display: flex;
justify-content: center;
flex-direction: row;
color: white ;
gap: 70px;
padding-block: 30px;
}

h5{
text-transform: uppercase;}

ul li{
text-transform: capitalize;
opacity: 90%;
}
ul li:hover{
color: #333333;
}

button:hover{
background-color: white;
color: black;
}
hr{
background-color: white;
}
.logo-container{
width: 80%;
margin: 0 auto;
justify-content: space-between;
color: white;
align-items: center;
padding-top: 20px;
    figure img{
    width: 200px;
    }
    span{
    text-transform: capitalize;
    }
}
.line{
height: 1px;
margin: 0 auto;
width: 80%;
background-color: white;
}
</style>
