<script setup lang="ts">
import { copyrightSign } from '../assets/icons';
import { footerLogo } from '../assets/images';
import { footerLinks, socialMedia } from '../constants';
</script>

<template>
    <footer class="max-container">
        <div class="flex justify-between items-start gap-20 flex-wrap max-lg:flex-col">
            <div class="flex flex-col items-start">
                <a href="/">
                    <img :src="footerLogo" width="150" height="50">
                </a>
                <p class="mt-6 text-base leading-7 font-montserrat text-white-400"> Get shoes ready for the new term at your nearest Nike store. Find your perfect size in store.</p>
                <div class="flex items-center gap-5 mt-8">
                    <div v-for="item in socialMedia" class="flex justify-center items-center w-12 h-12 bg-white rounded-full">
                        <img :src="item.src" :alt="item.alt" width="24" height="24">
                    </div>
                </div>
            </div>

            <div class="flex flex-1 justify-between lg:gap-10 gap-20 flex-wrap">
                <div v-for="(section, i) in footerLinks" :key="i" class="">
                    <h4 class="text-white font-montserrat text-2xl leading-normal font-medium mb-6">{{ section.title }}</h4>
                    <ul class="">
                        <li v-for="link in section.links" class="mt-3 text-white-400 font-montserrat text-base leading-normal hover:text-slate-gray cursor-pointer">
                            <a :href="link.link">{{ link.name }}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
        <div class="flex justify-between text-white-400 mt-24 max-sm:flex-col max-sm:items-center">
            <div class="flex flex-1 font-montserrat justify-start items-center gap-2 cursor-pointer">
                <img :src="copyrightSign" width="20" height="20" class="rounded-full m-0">
                <p>Copyright. All right reserved.</p>
            </div>
            <p class="cursor-pointer font-montserrat">Term & Conditions</p>
        </div>
    </footer>
</template>