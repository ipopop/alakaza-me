<template>
<div class="flex flex-wrap sm:flex-no-wrap mx-auto items-center overflow-hidden bg-white rounded-lg shadow-lg">
    <img class="object-center w-auto sm:w-72 h-auto" :src="destination.imageUrl" :alt="destination.imageAlt">
    <div class="object-center mx-auto my-auto sm:px-6 py-4 sm:w-48 sm:h-48">
        <h3 class="text-lg font-semibold text-gray-800">{{ destination.city }}</h3>
        <p class="text-gray-600">${{ destination.averagePrice }} / night
            <br class="inline" />
            <span>average</span>
        </p>
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
