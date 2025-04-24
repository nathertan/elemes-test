<template>
  <section class="hero">
    <div class="hero-wrapper">
      <div class="title-wrapper">
        <div class="title">
          Good Food Us <br />
          Good Mood
        </div>
        <div class="subtitle">
          I would think that conserving our natural <br />
          resources should be a conservative position: Not to waste food, and <br />
          not to throw away a lot of the food that we buy.
        </div>
        <div class="hero-button">
          <button class="hero-button-register">Daftar Sekarang</button>
          <button class="hero-button-about">About Us</button>
        </div>
      </div>

      <div class="hero-image">
        <img src="@/assets/header-food.svg" alt="hero-image" class="hero-image" />
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
.hero {
  background:
    linear-gradient(rgba(255, 255, 255, 0), rgba(255, 255, 255, 0)),
    url('@/assets/hero-background.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 100vw;
  height: 100vh;
}

.hero-wrapper {
  padding-top: 3vh;
  display: flex;
  flex-direction: row;
  justify-content: center;
  gap: 10vw;
}

.title-wrapper {
  padding-left: 7.5vw;
  padding-top: 25vh;
}

.title {
  font-weight: bold;
  font-size: 64px;
  color: #8bac3e;
  padding-bottom: 32px;
}

.subtitle {
  padding-bottom: 32px;
  font-weight: normal;
  font-size: 18px;
  line-height: 29px;
  color: #757575;
}

.hero-button-register {
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
  margin-right: 16px;
  box-shadow: 2px 5px 15px rgba(0, 0, 0, 0.5);
}

.hero-button-about {
  background-color: #f2f2f2;
  color: black;
  border: none;
  border-radius: 100px;
  cursor: pointer;
  padding: 10px 18px 10px 18px;
  white-space: nowrap;
  font-size: 14px;
  font-weight: bold;
  line-height: 22px;
  margin-right: 16px;
}

.hero-image {
  padding-top: 20px;
  width: 42vw;
}
@media (min-width: 1024px) {
}
</style>
