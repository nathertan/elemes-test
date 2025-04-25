<template>
  <section class="trending">
    <div class="trending-wrapper">
      <div class="title-wrapper">
        <div class="title">
          <span>Browser Our Category</span>
          <br />
          <span><font color="#8BAC3E">Trending</font></span>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Header',
})
</script>

<style scoped>
.trending {
  width: 100vw;
  height: 80vh;
  padding-left: 4.75vw;
  padding-right: 4.75vw;
}

.title-wrapper {
  padding-top: 10vh;
  padding-left: 7.5vw;
}

.title {
  font-size: 38px;
  line-height: 50px;
  padding-bottom: 32px;
  font-weight: bold;
}

@media (min-width: 1024px) {
}
</style>
