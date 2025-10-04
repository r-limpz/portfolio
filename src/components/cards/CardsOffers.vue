<template>
    <div class="flex justify-center space-x-10">
        <div v-for="offer in offers"
            class="w-64 h-96 max-h-[350px] border border-gray-500 rounded-lg shadow-sm hover:border-cyan-300 transition delay-150 duration-300 ease-in-out">
            <img :src="offer.image" alt="" class="h-48 w-auto rounded-t-lg object-cover"></img>
            <div class="space-y-8 p-4">
                <div class="">
                    <h5 class=" text-md font-bold text-center"> {{ offer.service }} </h5>
                </div>
                <p class=" text-sm text-gray-300 ">{{ offer.summary }}</p>
            </div>
        </div>
    </div>

</template>

<script setup>
const offers = [
  {
    name: "web_development",
    image: "markus-spiske-yPBgHCsKdWE-unsplash.jpg", // Replace with your actual image URL
    service: "Web Development",
    summary: "Building responsive, performant, and scalable websites.."
  },
  {
    name: "ui_ux_design",
    image: "hal-gatewood-xzzgY__zX8A-unsplash.jpg", // Replace with your actual image URL
    service: "UI & UX Design",
    summary: "Designing intuitive user interfaces and seamless user experiences."
  },
  {
    name: "web_design",
    image: "edho-pratama-T6fDN60bMWY-unsplash.jpg", // Replace with your actual image URL
    service: "Web Design",
    summary: "Creating visually appealing and brand-aligned website layouts."
  },
  {
    name: "hardware_it_support",
    image: "bermix-studio-SJwYvNVW1qY-unsplash.jpg", // Replace with your actual image URL
    service: "Hardware Tech / IT Support",
    summary: "Providing technical support and troubleshooting for hardware issues."
  }
]
</script>


<script>
export default {
    name: "CardsOffers"
}
</script>