<script setup lang="ts">
import { star } from '../assets/icons';

defineProps({
    thumbnail: { 
        type: String, 
        required: true 
    },
    name: { 
        type: String,
        required: true 
    },
    price: { 
        type: String, 
        required: true 
    },
    rating: {
        type: Number,
        required: true 
    }
});
</script>

<template>
    <div class="flex flex-1 flex-col w-full max-sm:w-full">
        <img
            :alt="name"
            width="280"
            height="280"
            class="object-contain"
            :src="thumbnail"
        />
        <div class="mt-8 gap-2.5 flex justify-start">
            <img 
                :src="star" 
                alt="Rating"
                width="22"
                height="22"
            />
            <p class="text-lg font-montserrat leading-normal text-slate-gray">({{ rating }})</p>
        </div>
        <h3 class="mt-2 text-2xl leading-normal font-semibold font-palanquin">{{ name }}</h3>
        <p class="mt-2 text-2xl font-montserrat font-semibold leading-normal text-coral-red">{{ price }}</p>
    </div>
</template>
