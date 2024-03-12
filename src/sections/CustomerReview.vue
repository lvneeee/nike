<script setup lang="ts">
import ReviewCard from '../components/ReviewCard.vue';
import { reviews } from '../constants';
</script>
<template>
    <section id="review" class="max-container">
        <h3 class="font-palanquin text-center text-4xl font-bold">
            What Our
            <span class="text-coral-red">Customers</span>
            Say?
        </h3>
        <p class="info-text m-auto mt-4 max-w-lg text-center">
            Hear genuine stories from our satisfied customers about their exceptional experiences with us.
        </p>
        <div class="mt-24 flex flex-1 justify-evenly items-center max-lg:flex-col gap-14">
            <ReviewCard v-for="(review, i) in reviews" :key="i" :avt="review.avt" :name="review.customerName" :rating="review.rating" :feedback="review.feedback"></ReviewCard>
        </div>
    </section>
</template>