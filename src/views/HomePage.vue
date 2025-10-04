<template>
    <div class=" space-y-20 flex-col relative h-screen overflow-auto">
        <section class="h-[90vh] max-h-[900px] w-auto max-w-[1080px] mx-auto grid">
            <div class="flex justify-between self-center space-x-10">
                <div class="space-y-10">
                    <div>
                        <h1 class="font-bold uppercase">
                            <p class="text-4xl"> Hello I am </p>
                            <p class=" text-cyan-300 text-7xl"> Rex Limpangog</p>
                        </h1>
                        <br />
                        <p class="text-gray-300">Junior Web Developer | Pragmatic </p>
                    </div>
                    <div class="flex justify-items-start space-x-6 items-center">
                        <Socials />
                        <Buttons @click="downloadPDF" class="bg-gray-950/60">
                            <span class="mx-4"> Download Resume
                                <i class="ml-2 fa-solid fa-download"></i>
                            </span>
                        </Buttons>
                    </div>
                </div>
                <div class="">
                    <img class="w-80 h-80 object-cover rounded-full border-gray-300" src="/me.png" alt="">
                </div>
            </div>
        </section>

        <section class="h-[70vh] max-h-[500px] w-auto max-w-[1080px] mx-auto self-center grid" id="services">
            <h1 class="text-center text-4xl font-bold"> Services Offer</h1>
            <CardsOffers />
        </section>

        <section class="h-[70vh] max-h-[350px] w-auto max-w-[1080px] mx-auto self-center grid" id="education">
            <h1 class="text-center text-4xl font-bold">Education</h1>
            <CardsEduc />
        </section>

        <section class="max-h-[900px] max-w-[1080px] mx-auto self-center grid" id="projects">
            <div class="p-5 flex justify-between items-center">
                    <span> Rex Limpangog</span>
                    <Socials />
            </div>
        </section>
    </div>
</template>

<script setup>
import pdfFile from '@/assets/files/Resume_Limpangog.pdf';

function downloadPDF() {
    const link = document.createElement('a');
    link.href = pdfFile;
    link.download = 'Resume.pdf';
    document.body.appendChild(link);
    link.click();
    document.body.removeChild(link);
}
</script>

<script>
import CardsEduc from '@/components/cards/CardsEduc.vue'
import Socials from '@/components/socials/Socials.vue'
import Buttons from '@/components/buttons/Buttons.vue'
import CardsOffers from '@/components/cards/CardsOffers.vue';


export default {
    name: "Home",
    components: {
        Buttons, Socials, CardsEduc
    }
}
</script>