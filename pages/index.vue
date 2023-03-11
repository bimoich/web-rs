<template>
    <div>
        <Swiper
            :modules="[SwiperAutoplay, SwiperEffectCreative, SwiperNavigation]"
            :slides-per-view="1"
            :loop="true"
            :effect="'creative'"
            :autoplay="{
                delay: 8000,
                disableOnInteraction: true,
            }"
            :creative-effect="{
                prev: {
                    shadow: false,
                    translate: ['-20%', 0, -1],
                },
                next: {
                    translate: ['100%', 0, 0],
                },
            }"
            :navigation="true"
        >
            <SwiperSlide v-for="(imageSlider, idx) in imageSliders" :key="idx">
                <img :src="`_nuxt/assets/img/${imageSlider}`" alt="" />
            </SwiperSlide>
        </Swiper>
        <h2>Homepage</h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, itaque dignissimos minus illum nostrum
            velit sequi odio molestiae culpa fuga?</p>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, itaque dignissimos minus illum nostrum
            velit sequi odio molestiae culpa fuga?</p>
    </div>
</template>

<script setup>
const imageSliders = [
    "Banner-MHBD-Now-Open.jpg",
    "IGD-banner-7c9d4.png",
]
</script>

<style scoped>
h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

p {
    margin: 20px 0;
}
</style>