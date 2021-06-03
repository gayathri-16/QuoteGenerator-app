<template>
  <div id="app">

     <link rel="preconnect" href="https://fonts.gstatic.com">
    <link href="https://fonts.googleapis.com/css2?family=Asul&family=Tangerine:wght@700&display=swap& family=Kodchasan:wght@200&family=Merienda&display=swap&family=Great+Vibes&family=ABeeZee:ital@1&family=Baloo+Tammudu+2&family=Mulish:wght@300&family=Tenali+Ramakrishna&display=swap" rel="stylesheet" />
   <link  rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.14.0/css/all.css" />
   <link href="https://fonts.googleapis.com/css2? family=Baloo+Thambi+2:wght@500&family=Montaga&family=Tajawal&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Libre+Baskerville:wght@700&display=swap" rel="stylesheet">
    <div class="first">
      <h1>FAMOUS QUOTES</h1>
       <div class="container">
            <div class="box">
                <div v-if="index < count" class="content">
                  <h2>" {{quotes[index]}} "</h2>
                  <button class="btn" @click="newQuote">- Rabindaranath Tagore</button>
              </div>
           </div>
       </div>
    </div>
     
  </div>
</template>

<script>

 

export default {
  name: 'App',
 
 
       data(){
        
            return{
              index:0,
              count:6,
             showTitle:false,
               quotes:[
                        
                        "It is very simple to be happy, but it is very difficult to be simple.",
                        "The highest education is that which does not merely give us information but makes our life in harmony with all existence.",
                        "The most important lesson that man can learn from life, is not that there is pain in this world, but that it is possible for him to transmute it into joy.",
                        "I slept and dreamt that life was joy. I awoke and saw that life was service. I acted and behold, service was joy.",
                        "If you cry because the sun has gone out of your life, your tears will prevent you from seeing the stars.",
                        "A lamp can only light another lamp when it continues to burn in its own flame."
                ],
                
                 }
            
        },
      methods:{
           
          newQuote()
          {
          this.index++
           
        }
      } 
       
    
}
</script>

<style>
body{
  display: flex;
  margin:0;
  padding:0;
  justify-content: center;
  align-items: center;
  height:auto;
  background:url("https://www.pixelstalk.net/wp-content/uploads/images4/Nature-Background-4K-2-scaled.jpg")
}

h1{
  color:black;
  text-align:center;
  font-family: 'Libre Baskerville', serif;
  margin-bottom:8rem;
  margin-top:2rem;
 transition:transform 100ms ease-in;
}
h1:hover{
   
   transform:scale(1.07);
}
.first{
  margin-bottom:15rem;
}
.container
{
  position:relative;
  width:200%;
  height:200%;
  display:grid;
  grid-template-rows: repeat(auto-fill, minmax(100px));
  grid-gap:0 40px;
  grid-template-columns:auto;
  margin-left:-25rem;
  margin-top:2rem;
 
}
.container .box:after{
  content: '';
  position:absolute;
  top:0;
  left:0;
  width:50%;
  height:100%;
  background: rgba(255,255,255,0.05);
}
.container .box:before{
  content:'';
  position:absolute;
  top:-2px;
  left: -2px;
  right:-2px;
  bottom: -2px;
  background: rgb(0, 0, 0);
  transform: skew(1deg,1deg);
  z-index:-1;
}
.container:hover .box:nth-child(1):before{
  background: linear-gradient(315deg,#ff0057,#e64a19);
}



.box{
  position:relative;
  height:230px;
  background:#020205;
  display: flex;
  justify-content:center;
  align-items:center;
  border:1px solid #000;
}
.content{
  position:relative;
  padding:20px;
  transform: translateY(40px);
}
h2{
margin-top:-2rem;
font-size:20px;
color:#fff;
text-align:left;
width:500px;
margin-left:-1rem;
line-height:40px;
letter-spacing: 1px;
word-spacing: 3px;
font-weight: lighter;
font-family: 'Merienda', cursive;

}
.box button{
  position:relative;
  margin:20px 0 20px;
  text-decoration: none;
  display:inline-block;
  color:#e7ebfa;
  transition: 0.7s;
  transform: translateY(-40px);
  opacity: 0;
  font-size:30px;
  font-weight:bold;
  font-family: 'Tangerine', cursive;
  background:transparent;
  border:none;
  margin-top:-2rem;
  margin-left:23rem;
   transition:transform 100ms ease-in;
}
.box:hover  button{
  transform: translateY(0);
  opacity: 1;
  visibility: visible;
  cursor:pointer;
 
    
}
button:hover{
  background: #fff;
  color:#061327;
  transform:scale(1.07);
 
}

</style>
