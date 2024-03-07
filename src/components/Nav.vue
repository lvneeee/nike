<script setup lang="ts">
import { headerLogo } from "../assets/images";
import { hamburger } from "../assets/icons";

import { navLinks, functionalMenu } from "../constants/index";
</script>

<template>
    <header class="absolue padding-x py-6 z-10 w-full">
        <nav class="flex justify-between items-center max-container">
            <a href="/">
                <img :src="headerLogo" alt="Logo" height="30" width="130" />
            </a>
            <ul
                class="flex-1 flex justify-center items-center gap-16 max-lg:hidden"
            >
                <li v-for="link in navLinks" :key="link.label" 
                    class="font-montserrat leading-normal text-lg text-slate-gray hover:text-black"
                >
                    <a
                        :href="link.href"
                        >{{ link.label }}</a
                    >
                </li>
            </ul>
            <ul
                class="flex justify-center items-center gap-4 max-lg:hidden"
            >
                <li v-for="functional in functionalMenu" :key="functional.label" class="after:content-['/'] after:text-black after:font-bold after:ml-4 last:after:hidden">
                    <a
                        :href="functional.href"
                        class="font-montserrat leading-normal text-lg text-black font-bold"
                        >{{ functional.label }}</a
                    >
                </li>
            </ul>
            <div class="hidden max-lg:block">
                <img :src="hamburger" alt="hamburger" height="25" width="25">
            </div>
        </nav>
    </header>
</template>
