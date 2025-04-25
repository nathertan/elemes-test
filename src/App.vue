<script setup lang="ts">
import Header from './components/Header.vue'
import HeroSection from './components/HeroSection.vue'
import Category from './components/Category.vue'
import Trending from './components/Trending.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="app-wrapper">
    <div>
      <Header></Header>
      <HeroSection />
    </div>

    <div>
      <Category />
    </div>

    <div>
      <Trending />
    </div>

    <div>
      <Footer></Footer>
    </div>

    <div class="watermark">© 2021 ELEMES ID. ALL RIGHTS RESERVED</div>
  </div>
</template>

<style scoped>
.app-wrapper {
  display: flex;
  flex-direction: column;
  width: 100vw;
  top: 0;
  left: 0;
  overflow-y: hidden;
}

.watermark {
  font-size: 12px;
  color: #757575;
  line-height: 16px;
  display: flex;
  align-self: center;
  padding-bottom: 30px;
}

@media (min-width: 1024px) {
}
</style>
