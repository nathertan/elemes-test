<template>
  <section class="trending">
    <div class="trending-wrapper">
      <div class="title-wrapper">
        <div class="title">
          <span>Browser Our Trending</span>
          <br />
          <span><font color="#8BAC3E">Receipt</font></span>
        </div>
      </div>

      <div class="display-wrapper">
        <div class="display">
          <div
            v-for="(card, index) in cards"
            :key="index"
            class="card"
            :style="{ '--card-color': card.bgColor }"
          >
            <img :src="card.image" alt="" class="card-image" />
            <div class="card-content">
              <span class="card-title">{{ card.title }}</span>
              <span class="card-desc"> {{ card.description }}</span>
              <img :src="card.rating" alt="" class="card-rating" />
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="button-wrapper">
      <button class="button-all-receipt">All Receipt</button>
    </div>
  </section>
</template>

<script setup lang="ts">
import paperoni from '@/components/icons/trending/paperoni.jpg'
import meat from '@/components/icons/trending/meat.jpg'
import doner from '@/components/icons/trending/doner.jpg'
import salmon from '@/components/icons/trending/salmon.jpg'
import cupcake from '@/components/icons/trending/cupcake.jpg'
import milk from '@/components/icons/trending/milk.jpg'
import unicorn from '@/components/icons/trending/unicorn.jpg'
import kathi from '@/components/icons/trending/kathi.jpg'
import threestar from '@/components/icons/rating/3-star.svg'
import fourstar from '@/components/icons/rating/4-star.svg'
import fivestar from '@/components/icons/rating/5-star.svg'

const cards = [
  {
    title: 'Pizza Paperoni',
    description: 'Pizza',
    image: paperoni,
    bgColor: '#E6F3F5',
    rating: fourstar,
  },
  {
    title: 'Pizza Meat',
    description: 'Pizza',
    image: meat,
    bgColor: '#E6F3F5',
    rating: threestar,
  },
  {
    title: 'Doner Kebab',
    description: 'Kebab',
    image: doner,
    bgColor: '#EAEEFA',
    rating: fivestar,
  },
  {
    title: 'Salmon Roll',
    description: 'Salmon',
    image: salmon,
    bgColor: '#F9EEF3',
    rating: fourstar,
  },
  {
    title: 'Cupcake Choco',
    description: 'Cupcake',
    image: cupcake,
    bgColor: '#F0FEEB',
    rating: fourstar,
  },
  {
    title: 'Doughnut Milk',
    description: 'Doughnut',
    image: milk,
    bgColor: '#F3F7D9',
    rating: fivestar,
  },
  {
    title: 'Doughnut Unicorn',
    description: 'Doughnut',
    image: unicorn,
    bgColor: '#F3F7D9',
    rating: fourstar,
  },
  {
    title: 'Kathi Kebab',
    description: 'Kebab',
    image: kathi,
    bgColor: '#EAEEFA',
    rating: fourstar,
  },
]
</script>

<style scoped>
.trending {
  width: 100;
  height: 120vh;
  padding-left: 4.75vw;
  padding-right: 4.75vw;
  margin-bottom: 12vh;
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

.display-wrapper {
  justify-content: center;
  padding-left: 7.5vw;
}

.display {
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  gap: 60px;
  width: calc(4 * (312.5px + 60px));
}

.card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 287.5px;
  height: 306px;
  border-radius: 15px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  background: var(--card-color);
  padding-left: 25px;
}

.card-image {
  height: 120px;
  width: 118.15px;
  border-radius: 6px;
  padding-bottom: 20px;
}

.card-content {
  display: flex;
  flex-direction: column;
}

.card-title {
  font-weight: bold;
  font-size: 26px;
  line-height: 50px;
}

.card-desc {
  font-weight: bold;
  font-size: 18px;
  color: #8bac3e;
}

.card-rating {
  padding-top: 5px;
  width: 68.23px;
  height: 10.66px;
}

.button-wrapper {
  margin-top: 80px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.button-all-receipt {
  background-color: #8bac3e;
  color: white;
  border: none;
  border-radius: 100px;
  cursor: pointer;
  padding: 10px 18px 10px 18px;
  font-size: 16px;
  font-weight: bold;
  line-height: 100%;
  width: 160px;
  height: 50px;
  margin-right: 20px;
}

@media (min-width: 1024px) {
}
</style>
