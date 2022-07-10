<template>
<header>
  <h1>{{mode}} Mode</h1>
  <toggle-comp :mode="mode" @toggle="$emit('toggle')"></toggle-comp>
  <nav>
    <div class="nav-link">Home</div>
    <div class="nav-link">About</div>
    <div class="nav-link">Portfolio</div>
    <div class="nav-link">Contact</div>
  </nav>
</header>
</template>

<script>
import ToggleComp from "@/components/ToggleComp";

export default {
  name: "HeaderComp",
  components: {ToggleComp},
  props: ['mode']
}
</script>

<style>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 25px;
  height: 60px;
  background-color: #c3c3c3;
  transition: background-color 0.3s ease-in-out;
}
.dark header {
  background-color: #15202b;
}

header h1 {
  font-size: 32px;
  text-transform: uppercase;
  font-weight: 900;
}

header nav {
  display: flex;
  height: 60px;
}

header nav .nav-link {
  display: flex;
  align-items: center;
  padding: 0 15px;
}

header nav .nav-link:hover {
  background-color: #b0b0b0;
}
.dark header nav .nav-link:hover {
  background-color: #101520;
}
</style>
