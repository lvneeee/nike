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
        <section class="padding">
            <Services />
        </section>
        <section class="padding">
            <SpecialOffer />
        </section>
        <section class="padding">
            <CustomerReview />
        </section>
        <section class="padding">
            <Subcribe />
        </section>
        <section class="padding">
            <Footer />
        </section>
    </main>
</template>

<style scoped></style>
