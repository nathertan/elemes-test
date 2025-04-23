<template>
  <header class="header">
    <div class="header-logo">Elemes.id</div>
    <nav class="header-nav">
      <a href="#" class="header-nav-link">Home</a>
      <a href="#" class="header-nav-link">About</a>
      <a href="#" class="header-nav-link">Promotions</a>
      <a href="#" class="header-nav-link">Blogs</a>
      <a href="#" class="header-nav-link">Contact Us</a>
    </nav>
    <div class="header-auth">
      <button class="header-auth-login">Masuk</button>
      <button class="header-auth-register">Daftar Sekarang</button>
    </div>
  </header>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Header',
})
</script>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
