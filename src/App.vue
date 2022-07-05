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
  <my-main :key="componentKey">
    <transition name="check">
      <div class="first"></div>
    </transition>
        <transition name="check2">
      <div class="first second"></div>
    </transition>
  </my-main>
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
  z-index: 1;
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
  animation: anim 5s ease;
  transform: translateY(-250px);
}

.second {
  transform: translateY(-400px);
  background-color: rgb(177, 150, 77);
  animation: anim2 5s ease;
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

</style>
