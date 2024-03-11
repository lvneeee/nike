<script setup lang="ts">

// import { defineProps } from 'vue';

defineProps({
    thumbnail: {
        type: String,
        required: true,
    },
    bigShoe: {
        type: String,
        required: true,
    },
});


</script>

<template>
    <div
        class="border rounded-xl cursor-pointer max-sm:flex-1"
        :class="{
            'border-coral-red': bigShoe === thumbnail,
            'border-transparent': bigShoe !== thumbnail
        }"
    >
        <img
            alt="shoe collection"
            width="127"
            height="103.34"
            class="object-contain"
            :src="thumbnail" 
        />
    </div>
</template>
