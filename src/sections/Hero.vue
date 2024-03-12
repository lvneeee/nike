<script setup lang="ts">
import { ref } from "vue";

import Button from "../components/Button.vue";
import ShoeCard from "../components/ShoeCard.vue";
import { arrowRight } from "../assets/icons";
import { statistics, shoes } from "../constants/index";

const selectedShoe = ref(shoes[0].bigShoe);

function changeBigShoeImg(bigShoe: string) {
    selectedShoe.value = bigShoe;
}
</script>

<template>
    <section
        id="home"
        class="w-full flex xl:flex-row flex-col justify-center min-h-screen gap-10 max-container "
    >
        <div
            class="relative xl:w-2/5 flex flex-col justify-center items-start w-full max-xl:padding-x pt-28"
        >
            <p class="text-xl font-montserrat text-coral-red">
                Our Summer Collection
            </p>
            <h1
                class="mt-10 font-palaquin font-bold text-8xl max-sm:text-[72px] max-sm:leading-[82px]"
            >
                <span
                    class="xl:bg-white xl:whitespace-nowrap relative z-10 pr-10"
                    >The New Arrival</span
                >
                <br />
                <span class="text-coral-red inline-block mt-3">Nike</span>
                Shoes
            </h1>
            <p
                class="font-montserrat text-slate-gray text-lg leading-8 mt-6 mb-14 sm:max-w-sm"
            >
                Discover stylish Nike arrivals, quality comfort, and innovation
                for your active life.
            </p>
            <Button :icon="arrowRight">Shop Now</Button>
            <div
                class="flex justify-start items-start flew-wrap w-full mt-20 gap-16"
            >
                <div v-for="(stas, i) in statistics" :key="i">
                    <p class="text-4xl font-bold font-palanquin">
                        {{ stas.value }}
                    </p>
                    <p class="leading-7 font-montserrat text-slate-gray">
                        {{ stas.label }}
                    </p>
                </div>
            </div>
        </div>
        <div
            class="relative flex-1 flex justify-center items-center xl:min-h-screen max-xl:py-40 bg-primary bg-hero bg-cover bg-center"
        >
            <img
                :src="selectedShoe"
                alt="shoe collection"
                width="610"
                height="502"
                class="object-contain relative z-10"
            />

            <div
                class="flex gap-4 absolute -bottom-[5%] sm:gap-6 sm:mx-auto max-sm:px-6"
            >
                <ShoeCard
                    v-for="(shoe, i) in shoes"
                    :key="i"
                    :thumbnail="shoe.thumbnail"
                    @click="() => changeBigShoeImg(shoe.bigShoe)"
                    :bigShoe="shoe.bigShoe"
                    :class="{
                        'border-coral-red': selectedShoe === shoe.bigShoe,
                        'border-transparent': selectedShoe !== shoe.bigShoe,
                    }"
                />
            </div>
        </div>
    </section>
</template>
