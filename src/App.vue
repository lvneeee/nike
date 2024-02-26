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
        <Nav />
        <section class="">
            <Hero />
        </section>
        <section class="">
            <PopularProducts />
        </section>
        <section class="">
            <SuperQuality />
        </section>
        <section class="">
            <Services />
        </section>
        <section class="">
            <SpecialOffer />
        </section>
        <section class="">
            <CustomerReview />
        </section>
        <section class="">
            <Subcribe />
        </section>
        <section class="">
            <Footer />
        </section>
    </main>
</template>

<style scoped></style>
