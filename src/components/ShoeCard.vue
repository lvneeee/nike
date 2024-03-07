<script setup lang="ts">
import { computed } from "vue";

interface ImgURL {
    thumbnail: string;
    bigShoe: string;
}

const props = defineProps({
    imgURL: {
        type: Object as () => ImgURL,
        required: true,
    },
    bigShoeImg: {
        type: String,
        required: true,
    },
});

const isBigShoe = computed(() => props.bigShoeImg === props.imgURL.bigShoe);

const handleClick = () => {
    if (!isBigShoe.value) {
        emit("change-big-shoe-image", props.imgURL.bigShoe);
    }
};

const emit  = defineEmits(["change-big-shoe-image"]);
</script>

<template>
    <div
        :class="`border-2 rounded-xl ${
            isBigShoe ? 'border-coral-red' : 'border-transparent'
        }`"
        class="cursor-pointer max-sm:flex-1"
        @click="handleClick"
    >
        <div
            class="flex justify-center items-center bg-card bg-center bg-cover sm:w-40 sm:h-40 rounded-xl max-sm:p-4"
        >
            <img
                :src="imgURL.thumbnail"
                alt="shoe collection"
                width="127"
                height="103.34"
                class="object-contain"
            />
        </div>
    </div>
</template>
