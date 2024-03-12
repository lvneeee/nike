<script setup lang="ts">
import { arrowRight } from '../assets/icons';
import { offer } from '../assets/images';
import Button from '../components/Button.vue';
</script>
<template>
    <section class="flex justify-wrap items-center max-xl:flex-col-reverse gap-10 max-container">
        <div class="flex-1">
            <img :src="offer" width="775" height="680" class="object-contain w-full ">
        </div>
        <div class="flex flex-1 flex-col">
            <h2
                class="font-palaquin capitalize font-bold text-4xl lg:max-w-lg"
            >
                <span class="text-coral-red">Special</span>
                Offer
            </h2>
            <p
                class="mt-4 info-text lg:max-w-lg"
            >
            Embark on a shopping journey that redefines your experience with unbeatable deals. From premier selections to incredible savings, we offer unparalleled value that sets us apart.
            </p>
            <p class="mt-6 lg:max-w-lg info-text">Navigate a realm of possibilities designed to fulfill your unique desires, surpassing the loftiest expectations. Your journey with us is nothing short of exceptional.</p>
            <div class="mt-11 flex flex-wrap gap-4">
                <Button :icon="arrowRight">Shop Now</Button>
                <Button var="ghost">Learn more</Button>
            </div>
        </div>
    </section>
</template>
