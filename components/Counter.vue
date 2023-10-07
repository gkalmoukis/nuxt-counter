<template>
    <div class="flex flex-col justify-center items-center h-screen">
        <div class="text-2xl font-semibold mb-4">
            {{ name1 }}  {{ name2 }}
        </div>
        <div class="mb-4 text-gray-600">
            {{ description }}
        </div>
        <div class="flex">
            <div class="mr-4 text-center">
                <div class="text-3xl font-semibold">{{ years }}</div>
                <div class="text-gray-600">Years</div>
            </div>
            <div class="mr-4 text-center">
                <div class="text-3xl font-semibold">{{ months }}</div>
                <div class="text-gray-600">Months</div>
            </div>
            <div class="mr-4 text-center">
                <div class="text-3xl font-semibold">{{ days }}</div>
                <div class="text-gray-600">Days</div>
            </div>
        </div>
        <div class="text-2xl font-semibold mt-3">
            {{ emoji }}
        </div>
    </div>
</template>

<script setup>
import moment  from 'moment';
import { ref, onMounted } from 'vue';

const name1 = "Name 1"
const name2 = "Name 2"
const description = "Mou are mouare ipsum dolor sit are, mu mouare elit."
const emoji = "❤️";
const pastDate = moment('2021-11-05T00:00:00');
const currentDate = moment();
const duration = moment.duration(currentDate.diff(pastDate));
const years = ref(duration.years());
const months = ref(duration.months());
const days = ref(duration.days());
</script>