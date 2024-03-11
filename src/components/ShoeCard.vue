<script setup lang="ts">

defineProps({
    thumbnail: {
        type: String,
        required: true
    },
    bigShoeImg: {
        type: String,
        required: true
    }
})

const handleClick = () => {
    if (bigShoeImg !== selectedShoe) 
}

</script>

<template>
    <div class="border-black border-2 rounded-xl cursor-pointer max-sm:flex-1"
        :class="`${bigShoeImg === seletedShoe ? 'border-coral-red' : 'border-transparent' }`"
        @click="handleClick"
        >
        <img
                :src="thumbnail"
                alt="shoe collection"
                width="127"
                height="103.34"
                class="object-contain"
            />
    </div>
</template>
