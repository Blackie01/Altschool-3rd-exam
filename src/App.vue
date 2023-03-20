<template>
  <!-- <router-link to="/counter"> <h1>sjhvskjf</h1> </router-link> -->
  <router-view />
  <CounterPage />

</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import CounterPage from './components/CounterPage.vue'
export default {
name: 'App',
components: {
  CounterPage,
}
}
</script>

<style>

html {
/* flex-direction: column; */
height: 100vh;
  display: grid;
  align-content: center;
  /* justify-content: center; */
  background-repeat:no-repeat;
  background-size: cover;
  background-position: center;
}
body {
background: linear-gradient(120deg, #272626 37%, #673736, #db5a56);
}


.jumboName {
  font-size: 100px;
  margin-left: 90px;
  color: #db5a56;
}

.dot {
  color: #774140;
}

#tagline {
  margin-top: -80px;
  margin-left: 92px;
}

#app {
font-family: Avenir, Helvetica, Arial, sans-serif;
-webkit-font-smoothing: antialiased;
-moz-osx-font-smoothing: grayscale;
text-align: center;
color: #2c3e50;
/* background-color: #012928ff; */
/* background-color: blue; */
/* margin-top: 60px; */
  width: 53%;
  height: 18em;
  /* padding: 2px 0 5px 0; */
  position: relative;
  left: 40%;
  bottom: 25%;
  /* width: 125%; */
}

h1, h3 {
color: #eedada;
}

@media screen and (max-width: 768px) {

  
  html {
    display: block;
  }

body {
  background-repeat:no-repeat;
  background-size: cover;
  background-position: center;
  margin: 35% auto auto auto;
  
}
#app {
  width: 100vw;
  left: 0;

}

.headerContent {
  text-align: center;
  margin-bottom: 50px;
}

.jumboName {
  font-size: 50px;
  margin-left: unset;
  color: #db5a56;
  text-align: center;
}

.dot {
  color: #774140;
}

#tagline {
  margin-top: -40px;
  margin-left: unset;
}
}
</style>