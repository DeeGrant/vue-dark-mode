<template>
<section class="content">
<div>
  <h3>This is {{mode}} mode</h3>
  <div class="image-grid">
    <div class="col">
      <img src="https://images.unsplash.com/photo-1560617137-b2bbe0e08397?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1200&h=600&fit=crop&ixid=eyJhcHBfaWQiOjF9" alt="">
    </div>
    <div class="col">
      <img src="https://images.unsplash.com/photo-1561327712-2e0c75a1a6e6?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1200&h=600&fit=crop&ixid=eyJhcHBfaWQiOjF9" alt="">
    </div>
    <div class="col">
      <img src="https://images.unsplash.com/photo-1560945928-a97ecc4dcfc7?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1200&h=600&fit=crop&ixid=eyJhcHBfaWQiOjF9" alt="">
    </div>
  </div>
  <p class="para">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
</div>
</section>
</template>

<script>
export default {
  name: "ContentComp",
  props: ['mode']
}
</script>

<style>
.content {
  padding: 25px;
}
.content h3 {
  font-size: 28px;
  text-transform: uppercase;
  font-weight: 300;
  margin-bottom: 25px;
}

.image-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 15px;
}
.image-grid .col img {
  width: 100%;
}

.para {
  width: 100%;
  max-width: 600px;
  margin: 25px auto 0;
}
</style>
