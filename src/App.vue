<template>
<div id="app">
    <div class="hidden p-3 bg-white">
        <h5 class="font-bold text-center text-blue-400">My New Tailwind Project</h5>
        <p class="italic font-bold text-center text-gray-500">(from tailwindcss.com/course)</p>
    </div>
    <div class="flex bg-gray-200">
        <div class="max-w-md px-8 py-4 mx-auto sm:py-12 sm:max-w-xl lg:max-w-full lg:w-1/2 lg:py-24 lg:px-12">
            <div class="xl:max-w-lg xl:ml-auto">
                <img class="h-10" src="img/logo.svg" alt="Workcation" />
                <img class="object-cover object-center w-full h-48 mt-6 rounded-lg shadow-xl sm:mt-8 sm:h-72 sm:object-cover lg:hidden" src="img/beach-work.jpg" alt="Woma Workcationing on the beach" />
                <h2 class="mt-6 text-2xl font-bold leading-tight text-gray-900 sm:text-4xl sm:mt-8 lg:text-3xl">
                    You can work from anywhere.
                    <br class="sm:hidden lg:inline" />
                    <span class="text-indigo-500">Take advantage of it.</span>
                </h2>
                <p class="mt-2 text-gray-600 sm:mt-4 sm:text-xl">
                    Workcation helps you find work-friendly rentals in beautiful
                    locations so you can enjoy som nice weather even when you're not on
                    vacation.
                </p>
                <div class="text-center sm:text-left my-8 sm:mt-6 sm:text-base xl:mt-10 xl:text-sm">
                    <a href="#" class="mb-6 shadow-lg btn btn-indigo w-full sm:w-auto">Book your escape</a>
                    <br class="sm:hidden inline" />
                    <a href="#dest" class="w-full sm:w-auto sm:ml-4 btn btn-gray">Learn more</a>
                </div>
            </div>
        </div>
        <div class="hidden lg:block lg:w-1/2 lg:relative">
            <img class="absolute inset-0 object-cover object-center w-full h-full" src="img/beach-work.jpg" alt="Woma Workcationing on the beach" />
        </div>
    </div>
    <div>
        <div class="max-w-md px-8 py-8 mx-auto sm:max-w-xl lg:max-w-6xl lg:px-12">
            <h2 id="dest" class="text-xl text-gray-900">Popular destinations</h2>
            <p class="text-gray-600">
                A selection of great work-friendly cities with lots to see and
                explore.
            </p>
            <div class="flex flex-wrap text-center">
                <div class="object-center mx-auto max-w-350 min-h-300 sm:max-w-450 px-4 mt-10" v-for="destination in popularDestinations" v-bind:key="destination">
                    <DestinationCard :destination="destination" />
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
import DestinationCard from "./components/DestinationCard";

export default {
    name: "app",
    components: {
        DestinationCard,
    },
    data() {
        return {
            popularDestinations: [{
                    city: "Toronto",
                    averagePrice: 120,
                    propertyCount: 76,
                    imageUrl: "img/toronto.jpg",
                    imageAlt: "Toronto skyline",
                },
                {
                    city: "Malibu",
                    averagePrice: 215,
                    propertyCount: 43,
                    imageUrl: "img/malibu.jpg",
                    imageAlt: "Cliff in Malibu",
                },
                {
                    city: "Chicago",
                    averagePrice: 130,
                    propertyCount: 115,
                    imageUrl: "img/chicago.jpg",
                    imageAlt: "Chicago skyline",
                },
                {
                    city: "Seattle",
                    averagePrice: 135,
                    propertyCount: 63,
                    imageUrl: "img/seattle.jpg",
                    imageAlt: "Seattle skyline",
                },
                {
                    city: "Colorado",
                    averagePrice: 85,
                    propertyCount: 47,
                    imageUrl: "img/colorado.jpg",
                    imageAlt: "Lake in Colorado",
                },
                {
                    city: "Miami",
                    averagePrice: 115,
                    propertyCount: 86,
                    imageUrl: "img/miami.jpg",
                    imageAlt: "Beach in Miami",
                },
            ],
        };
    },
};
</script>

<style src="./assets/tailwind.css"></style>
