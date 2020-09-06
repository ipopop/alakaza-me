<template>
  <div class="flex items-center overflow-hidden bg-white rounded-lg shadow-lg">
    <img class="flex-shrink-0 w-32 h-32" :src="destination.imageUrl" :alt="destination.imageAlt">
    <div class="px-6 py-4">
      <h3 class="text-lg font-semibold text-gray-800">{{ destination.city }}</h3>
      <p class="text-gray-600">${{ destination.averagePrice }} / night average</p>
      <div class="mt-4">
        <a href="#" class="text-sm font-semibold text-indigo-500 hover:text-indigo-400">Explore {{ destination.propertyCount }} properties</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['destination'],
}
</script>
