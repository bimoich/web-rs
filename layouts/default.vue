<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="nav-bar">
                <a href="/" class="home-btn">Website X</a>
                <div class="flex-row">
                    <ul class="flex gap-12">
                        <NuxtLink class="nav-link" to="/">About</NuxtLink>
                        <NuxtLink class="nav-link" to="/about">Medical Checkup</NuxtLink>
                        <NuxtLink class="nav-link" to="/products">Promo & News</NuxtLink>
                        <div>
                            <label>Follow us: </label>
                            <a v-for="link in socialLinks" :key="link.name" :href="link.url" target="blank" class="mx-3">
                                <font-awesome-icon :icon="['fa-brands', link.icon]" class="social-icons" />
                            </a>
                        </div>
                        <a href="https://www.google.com" class="contact-us-btn" target="_blank">
                            <font-awesome-icon icon="fa-solid fa-phone" /> Contact Us
                        </a>
                    </ul>
                    <ul class="flex gap-12">
                        <NuxtLink class="nav-link" to="/">Home</NuxtLink>
                        <NuxtLink class="nav-link" to="/about">Find a doctor</NuxtLink>
                        <NuxtLink class="nav-link" to="/products">Book appointment</NuxtLink>
                        <NuxtLink class="nav-link" to="/products">Hospitals</NuxtLink>
                        <NuxtLink class="nav-link" to="/products">Center of excellence</NuxtLink>
                    </ul>
                </div>
            </nav>
        </header>

        <!-- page content -->
        <div class="content-container">
            <slot />
        </div>
    </div>
</template>

<style scoped>
/* .router-link-exact-active {
    @apply text-[#12b488] rounded-md text-base;
} */
</style>

<script setup>
import { socialLinks } from 'assets/constants'
</script>
