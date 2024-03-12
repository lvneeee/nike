<script setup lang="ts">
import ServiceCard from '../components/ServiceCard.vue';
import { services } from '../constants';
</script>
<template>
    <section class="max-container flex justify-center flex-wrap gap-9">
        <ServiceCard v-for="(service, i) in services" :key="i" :icon="service.icon" :label="service.label" :subtext="service.subtext"></ServiceCard>
    </section>
</template>