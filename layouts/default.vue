<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="nav-bar">
                <a href="/" class="home-btn">Website X</a>
                <!-- <NuxtLink to="/" class="home-btn">Website X</NuxtLink> -->
                <ul class="flex gap-4">
                    <li><NuxtLink to="/">Home</NuxtLink></li>
                    <li><NuxtLink to="/about">About</NuxtLink></li>
                    <li><NuxtLink to="/products">Products</NuxtLink></li>
                </ul>
            </nav>
        </header>

        <!-- page content -->
        <div class="content-container">
            <slot />
        </div>
    </div>
</template>

<style scoped>
.router-link-exact-active {
    @apply bg-[#12b488] text-white px-3 py-2 rounded-md text-sm;
}
</style>
