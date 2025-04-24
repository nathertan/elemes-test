<template>
  <header class="header">
    <div class="header-logo">
      <img src="@/assets/Elemes-logo.svg" alt="elemes-logo" />
    </div>
    <nav class="header-nav">
      <a href="#" class="header-nav-link">Home</a>
      <a href="#" class="header-nav-link">About</a>
      <a href="#" class="header-nav-hot">
        Promotions
        <span class="hot-popup">HOT</span>
      </a>
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
.header {
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  padding: 2vh;
}

.header-logo {
  margin-left: 10vw;
  width: 207px;
}

.header-nav {
  justify-content: space-between;
  align-self: center;
}

.header-nav-link {
  padding-left: 16px;
  padding-right: 16px;
  font-weight: bold;
  color: #757575;
}

.header-nav-hot {
  padding-left: 16px;
  padding-right: 16px;
  font-weight: bold;
  color: #757575;
  position: relative;
}

.hot-popup {
  position: absolute;
  top: -0.8rem;
  background-color: #f44336;
  color: white;
  padding: 0.15rem 0.4rem;
  right: 5px;
  font-size: 0.6rem;
  border-radius: 10px;
  font-size: 8px;
  font-weight: lighter;
}

.header-auth {
  display: flex;
  align-items: center;
  margin-right: 10vw;
  width: 215px;
  gap: 24px;
}

.header-auth-login {
  background: none;
  border: none;
  color: #333;
  cursor: pointer;
  font-weight: bold;
  font-size: 14px;
}

.header-auth-register {
  background-color: #8bac3e;
  color: white;
  border: none;
  border-radius: 100px;
  cursor: pointer;
  padding: 10px 18px 10px 18px;
  white-space: nowrap;
  font-size: 14px;
  font-weight: bold;
  line-height: 22px;
}

@media (min-width: 1024px) {
}
</style>
