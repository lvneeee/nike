<script setup lang="ts">
import { computed } from "vue";

const props = defineProps({
    var: {
        type: String,
        default: "primary",
        validator: (value: string) => {
            return ["primary", "secondary", "success"].includes(value);
        },
    },
    icon: {
        type: String,
    },
});

const buttonClasses = computed(() => {
    let classes = "button ";
    if (props.var === "primary") {
        classes += "bg-coral-red text-white border-coral-red";
    } else if (props.var === "secondary") {
        classes += "bg-gray-600 text-white";
    } else if (props.var === "outline") {
        classes += "border-coral-red text-black";
    }
    return classes;
});
</script>

<template>
    <button
        :class="buttonClasses"
        @click="$emit('click')"
        class="flex justify-center items-center gap-2 px-7 py-4 boder font-montserrat text-lg leading-none rounded-full"
    >
        <slot></slot>
        <img :src="icon" alt="" class="ml-2 rounded-full w-5 h-5" />
    </button>
</template>
