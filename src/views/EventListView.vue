<script setup>
import EventCard from '@/components/EventCard.vue'
import { ref } from 'vue'
const events = ref([
  {
    id: 5928101,
    category: 'animal welfare',
    title: 'cat adoption day',
    description: 'find your new feline friend at this event',
    location: 'meow town',
    date: 'January 28 2024',
    time: '12:00',
    petsAllowed: true,
    organizer: 'Kat Laydee'
  },
  {
    id: 5928102,
    category: 'animal welfare',
    title: 'cat adoption day',
    description: 'find your new feline friend at this event',
    location: 'meow town',
    date: 'January 29 2024',
    time: '13:00',
    petsAllowed: true,
    organizer: 'Kat Laydee'
  }
])
</script>

<template>

  <div class="events"><EventCard v-for="event in events" :key="event.id" :event="event" /></div>
</template>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}

h1 {
  font-size: 20px;
}
</style>
