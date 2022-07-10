<template>
  <div class="app" :class="mode">
    <header-comp :mode="mode" @toggle="toggle"></header-comp>
  </div>
</template>

<script>
import HeaderComp from "@/components/HeaderComp";

export default {
  name: 'App',
  data () {
    return {
      mode: 'light'
    }
  },
  components: {
    HeaderComp
  },
  methods: {
    toggle() {
      if(this.mode === 'dark') {
        this.mode = 'light'
      } else {
        this.mode = 'dark'
      }
    }
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

.app {
  width: 100vw;
  min-height: 100vh;
  background-color: #f3f3f3;
  color: #15202b;
  transition: background-color 0.3s ease-in-out;
}

.dark {
  background-color: #192734;
  color: #f3f3f3;
}

/*#app {*/
/*  font-family: Avenir, Helvetica, Arial, sans-serif;*/
/*  -webkit-font-smoothing: antialiased;*/
/*  -moz-osx-font-smoothing: grayscale;*/
/*  text-align: center;*/
/*  color: #2c3e50;*/
/*  margin-top: 60px;*/
/*}*/
</style>
