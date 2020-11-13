<template>
  <div id="counter">
    <h2>counter-vue</h2>
    <div class="number-grid">
      <div class="number">{{ number }}</div>
      <div class="buttons">
        <a href="#" @click="plusOne">↑</a>
        <a href="#" @click="minusOne" v-if="number > 0">↓</a>
      </div>
    </div>
  </div>
  <footer>
    <p>Made with 💚 using vue.js.</p>
    <a href="https://vuejs.org/"
      ><img id="logo" src="./assets/logo.png" alt=""
    /></a>
  </footer>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      number: 0,
    };
  },

  methods: {
    plusOne() {
      this.number++;
    },
    minusOne() {
      this.number--;
    },
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;

  font-size: 62.5%;
}

body {
  background: linear-gradient(to right, #d13b00, #084644);
}
#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  height: 100vh;
  width: 100vw;

  font-family: "Roboto", sans-serif;
}

#counter {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;

  height: 60vh;
  width: 40vw;
  border-radius: 2rem;

  background: rgba(11, 74, 132, 0.3);
}
#counter h2 {
  font-size: 4.5rem;
  padding-top: 3rem;
  font-weight: 300;
}

#counter .number-grid {
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 400;
  padding-bottom: 6rem;
}

.number-grid .buttons {
  font-size: 8rem;
  width: 6rem;
  display: flex;
  flex-direction: column;

  align-items: space-around;
  justify-content: center;
}

.number-grid .buttons a {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;

  text-decoration: none;
  font-size: 6rem;
  background: #18443e;
  color: white;
  margin: 0.5rem;
  border-radius: 1rem;
}

.number-grid .number {
  min-width: 15rem;
  font-size: 10rem;
  padding-right: 4rem;
}

footer {
  font-size: 2rem;
  position: absolute;
  bottom: 3rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

#logo {
  padding-left: 2.5rem;
  max-width: 6rem;
}
</style>
