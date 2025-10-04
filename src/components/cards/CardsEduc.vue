<template>
    <div class="flex justify-center space-x-10">
        <div v-for="edu in educ"
            class=" h-48 max-h-[180px] p-5 border border-gray-500 rounded-lg shadow-sm">
            <div class=" space-y-8">
                <div class="">
                    <h5 class="mb-2 text-md font-bold tracking-tight"> {{ edu.course }} </h5>
                    <p class="text-sm text-gray-400 "> {{ edu.schoolyear_start }} - {{ edu.schoolyear_end }} </p>
                </div>
                <p class=" text-sm text-gray-300 ">{{ edu.school }}</p>
            </div>
        </div>
    </div>

</template>

<script setup>
const educ = [
    { course: "ICT - Computer Systems Servicing ", schoolyear_start: "June 2014", schoolyear_end: "April 2020", school: "Calinan National High School" },
    { course: "Bachelor in Information Technology", schoolyear_start: "September 2020", schoolyear_end: "August 2024", school: "University of Southeastern Phillippines" }
]
</script>

<script>
export default {
    name: "CardsEduc"
}
</script>