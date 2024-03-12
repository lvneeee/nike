<script setup lang="ts">
import {
    Hero,
    PopularProducts,
    SuperQuality,
    Services,
    SpecialOffer,
    CustomerReview,
    Subcribe,
    Footer,
} from "./sections";
import Nav from './components/Nav.vue';
</script>

<template>
    <main class="relative">
        <Nav class="absolute top-0" />
        <section class="xl:padding-l wide:padding-r padding-b">
            <Hero />
        </section>
        <section class="padding">
            <PopularProducts />
        </section>
        <section class="padding">
            <SuperQuality />
        </section>
        <section class="padding-x py-10">
            <Services />
        </section>
        <section class="padding">
            <SpecialOffer />
        </section>
        <section class="bg-pale-blue padding">
            <CustomerReview />
        </section>
        <section class="padding-x sm:py-32 py-16 w-full">
            <Subcribe />
        </section>
        <section class="padding-x padding-t pb-8 bg-black">
            <Footer />
        </section>
    </main>
</template>

<style scoped></style>
