<script>

 export default {
  data() {
    return {
      componentKey: 0,
    };
  },
 }
</script>

<template>
  <header>
    <button @click="componentKey++">Reset</button>
  </header>
  <main :key="componentKey">
      <div class="first"></div>
      <div class="second"></div>
      <div class="ball-cover">
        <div class="ball"></div>
      </div>
      <div class="triangle"></div>
      <div class="rocket"> 
        <div class="top"></div>
        <div class="rocket-body"></div>
        <div class="window"></div>
        <div class="flame1"></div>
        <div class="flame2"></div>
      </div>
  </main>
  <footer>
  </footer>
</template>

<style>

body {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  margin: 0;
  background: #e9e9e9;
}


header {
  width: 40%;
  height: 70px;
  padding-top: 10px;
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
  background-color: #a7da93;
  margin: auto;
}

button {
  background-color: #76aae2;
  border-radius: 20px;
  border: 0px;
  font-size: large;
  font-weight: bold;
  color:#2a3f76;
  height: 80%;
  width: 200px;
}

button:hover {
  border: solid 5px;
  border-color: #76aae2;
  background-color: #7691e2;
  color:#2a3276;
}

button:active {
    Yborder: solid 5px;
  border-color: #76aae2;
  background-color: #5553a0;
  color:#000000;
}

footer {
  position: absolute;
  bottom: 0;
  height: 63px;
  width: 100%;
  background-color: #a7da93;
}


.first {
  margin: auto;
  width: 100px;
  height: 150px;
  background-color: rgb(124, 81, 165);
  animation: anim 4s ease;
  transform: translateY(-250px);
}

.second {
  margin: auto;
  width: 150px;
  height: 150px;
  transform: translateY(-400px);
  background-color: rgb(177, 150, 77);
  animation: anim2 4s ease;
}

.ball {
  margin: auto;
  width: 100px;
  height: 100px;
  border-radius: 50%;
  transform: translateY(-550px);
  background-color: rgb(210, 40, 31);
  animation: ball 4s linear;
}

.ball-cover {
  margin: auto;
  width: 100px;
  height: 100px;
  border-radius: 50%;
  transform: translateY(-550px);
  animation: ball-cover 4s linear;
}

.triangle {
  margin: auto;
  width: 0; 
  height: 0; 
  border-left: 50px solid transparent;
  border-right: 50px solid transparent;
  border-top: 50px solid rgb(13, 113, 206);
  animation: triangle 4s linear;
  transform: translateY(-700px);
}

.rocket {
  margin: auto;
  transform: translateY(-700px);
  animation: rocket 4s ease;
}

.top {
  margin: auto;
  width: 0; 
  height: 0; 
  border-left: 30px solid transparent;
  border-right: 30px solid transparent;
  border-bottom: 30px solid rgb(202, 39, 17);
  /* transform: translateY(-700px); */
}

.rocket-body {
  margin: auto;
  width: 60px;
  height: 60px;
  background-color:rgb(78, 56, 136);
}

.window {
  margin: auto;
  width: 15px;
  height: 25px;
  border: solid;
  border-radius: 50%;
  transform: translateY(-50px);
  background-color: rgb(49, 211, 252);
  border-color: #000000;
}

.flame2 {
  margin: auto;
  width: 0; 
  height: 0; 
  border-left: 10px solid transparent;
  border-right: 10px solid transparent;
  border-top: 10px solid rgb(240, 67, 19);
  transform: translateY(-56px);
}

.flame1 {
  margin: auto;
  width: 0; 
  height: 0; 
  border-left: 25px solid transparent;
  border-right: 25px solid transparent;
  border-top: 25px solid rgb(240, 211, 19);
  transform: translateY(-31px);
}


  

@keyframes anim {
  0% { transform: translateY(-250px); }
  25% {transform: rotate(180deg); }
  50% { transform: translateY(650px);  opacity: 1;}
  100% { transform: translateX(40vw) translateY(400px); opacity: 0; }
}

@keyframes anim2 {
  0% { transform: translateY(-400px); }
  50% { transform: translateY(500px) rotate(180deg); opacity: 1; }
  100% { transform: translateX(-40vw); opacity: 0; }
}


@keyframes ball {
  28% { transform: translateY(0px); width: 100px; height: 100px;}
  30% { transform: translateY(0px); width: 120px; height: 70px;}
  32% { transform: translateY(0px); width: 100px; height: 100px;}
  48% { transform: translateY(0px); width: 100px; height: 100px;}
  50% { transform: translateY(0px); width: 120px; height: 70px;}
  52% { transform: translateY(0px) translateX(0vw); width: 100px; height: 100px; opacity: 1;}
  100% { transform: translateX(0vw) translateY(0px); opacity: 0;}
}

@keyframes ball-cover {
  0% { transform: translateY(-550px); }
  10% { transform: translateY(-300px); }
  20% { transform: translateY(50px); }

  28% { transform: translateY(400px); }
  30% { transform: translateY(430px); }
  32% { transform: translateY(400px); }

  34% { transform: translateY(250px); }
  40% { transform: translateY(150px); }
  45% { transform: translateY(250px); }
  
  48% { transform: translateY(400px);}
  50% { transform: translateY(430px);}
  52% { transform: translateY(400px) translateX(0vw); opacity: 1;}

  100% { transform: translateX(40vw) translateY(400px); opacity: 0;}
}

@keyframes triangle {
  0% {transform: translateY(-700px); }
  50% { transform: translateY(350px) rotate(0deg); }
  60% { transform: translateY(356px) translateX(-20px) rotate(-45deg); opacity: 1; }
  100% { transform: translateY(356px) translateX(-40vw)  rotate(-45deg); opacity: 0; }
}

@keyframes rocket {
  0% {transform: translateY(-700px); }
  20% { transform: translateY(260px); }
  50% { transform: translateY(260px); opacity: 1;}
  100% { transform: translateY(-400px); opacity: 0; }
}

</style>
