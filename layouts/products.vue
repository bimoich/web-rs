<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 px-48">
                <NuxtLink to="/" class="home-btn">Website X Merch</NuxtLink>
            </nav>
        </header>

        <!-- page content -->
        <div class="content-container">
            <slot />
        </div>

        <footer class="container mx-auto p-4 flex justify-between border-t-2 px-48">
            <ul class="flex gap-4">
                <li>
                    <NuxtLink to="/">Home</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/about">About</NuxtLink>
                </li>
                <li>
                    <NuxtLink to="/products">Products</NuxtLink>
                </li>
            </ul>
        </footer>
    </div>
</template>

<style scoped>
.router-link-exact-active {
    @apply bg-[#12b488] text-white px-3 py-2 rounded-md text-sm;
}
</style>
