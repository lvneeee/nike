<script setup lang="ts">

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
    <div class="p-4 border-2 bg-card bg-center bg-cover rounded-xl cursor-pointer max-sm:flex-1"
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
