<template>
  <section class="category">
    <div class="category-wrapper">
      <div class="title-wrapper">
        <div class="title">
          <span>Browser Our Category</span>
          <br />
          <span><font color="#8BAC3E">Receipt</font></span>
        </div>
      </div>

      <div class="carousel-wrapper">
        <div class="carousel-scroll" ref="carouselRef">
          <div class="carousel-track">
            <div
              v-for="(card, index) in displaycard"
              :key="index"
              class="card"
              :style="{ '--card-color': card.bgColor }"
            >
              <img :src="card.image" alt="" class="card-image" />
              <div class="card-content">
                <span class="card-title">{{ card.title }}</span>
                <span class="card-desc"> {{ card.description }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="carousel-nav">
        <img src="@/components/icons/prev.png" @click="scroll('left')" />
        <img src="@/components/icons/next.png" @click="scroll('right')" />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'
import cupcake from '@/components/icons/category/cupcake.svg'
import pizza from '@/components/icons/category/pizza.svg'
import kebab from '@/components/icons/category/kebab.svg'
import salmon from '@/components/icons/category/salmon.svg'
import doughnut from '@/components/icons/category/doughnut.svg'

const cards = [
  {
    title: 'Cupcake',
    description: '22 items',
    image: cupcake,
    bgColor: '#F0FEEB',
  },
  {
    title: 'Pizza',
    description: '25 items',
    image: pizza,
    bgColor: '#E4F2F4',
  },
  {
    title: 'Kebab',
    description: '12 items',
    image: kebab,
    bgColor: '#EAEEFA',
  },
  {
    title: 'Salmon',
    description: '22 items',
    image: salmon,
    bgColor: '#F9EEF3',
  },
  {
    title: 'Doughnut',
    description: '11 items',
    image: doughnut,
    bgColor: '#F3F7D9',
  },
]
const displaycard = ref([...cards, ...cards])

const carouselRef = ref<HTMLDivElement | null>(null)
const cardWidth = 230 + 16 // Card width + gap (adjust to match your CSS)

// Main scroll function for buttons
const scroll = (direction: 'left' | 'right') => {
  if (!carouselRef.value) return

  const scrollAmount = cardWidth * 2 // Scroll 2 cards at a time
  const containerWidth = carouselRef.value.offsetWidth

  let newPosition =
    direction === 'left'
      ? carouselRef.value.scrollLeft - scrollAmount
      : carouselRef.value.scrollLeft + scrollAmount

  // Immediate scroll (no animation - better for infinite)
  carouselRef.value.scrollLeft = newPosition

  // Infinite scroll check (runs after 10ms)
  setTimeout(() => {
    if (!carouselRef.value) return

    const maxScroll = carouselRef.value.scrollWidth - containerWidth
    const tolerance = 10 // Pixel buffer

    if (carouselRef.value.scrollLeft <= tolerance) {
      // Jump to near end if at start
      carouselRef.value.scrollLeft = maxScroll - scrollAmount
    } else if (carouselRef.value.scrollLeft >= maxScroll - tolerance) {
      // Jump to near start if at end
      carouselRef.value.scrollLeft = scrollAmount
    }
  }, 10)
}

onMounted(() => {
  if (carouselRef.value) {
    // Start slightly offset to enable immediate left scroll
    carouselRef.value.scrollLeft = 0
  }
})
</script>

<style scoped>
.category {
  width: 100;
  height: 60vh;
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

.carousel-wrapper {
  max-width: 80vw;
  padding-top: 10px;
  padding-bottom: 10px;
  padding-left: 7.5vw;
  padding-right: 7.5vw;
}

.carousel-scroll {
  overflow: hidden;
  scroll-behavior: smooth;
  -ms-overflow-style: none;
  scrollbar-width: none;
  padding-top: 10px;
  padding-bottom: 10px;
}

.carousel-scroll::-webkit-scrollbar {
  display: none;
}

.carousel-track {
  width: max-content;
  display: flex;
  gap: 16px;
  flex-wrap: nowrap;
}

.card {
  width: 230px;
  height: 175px;
  border-radius: 15px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  transition:
    transform 0.3s ease,
    background-image 0.3s ease;
  flex-shrink: 0;
  cursor: pointer;
  gap: 20px;
  background: var(--card-color);
}

.card:hover {
  transform: scale(1.05);
  /* background: var(--card-color) url('../assets/hero-background.jpg') center/cover no-repeat; */
}

.card:hover::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: url('../assets/hero-background.jpg') center/cover no-repeat;
  opacity: 0.3; /* Adjust transparency (0.3 = 30% visible) */
  pointer-events: none; /* Allows clicks to pass through overlay */
}

.card-image {
  width: 47px;
  height: auto;
  object-fit: cover;
}

.card-content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.card-title {
  font-weight: bold;
  font-size: 16px;
}

.card-desc {
  font-size: 14px;
}

.carousel-nav {
  margin-top: 5vh;
  cursor: pointer;
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  padding-right: 7.5vw;
  gap: 10px;
}

@media (min-width: 1024px) {
}
</style>
