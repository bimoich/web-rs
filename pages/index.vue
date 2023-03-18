<template>
    <div>
        <section class="swiper-container">
            <Swiper :modules="[SwiperAutoplay, SwiperEffectCreative, SwiperNavigation]" :slides-per-view="1" :loop="true"
                :effect="'creative'" :autoplay="{
                    delay: 8000,
                    disableOnInteraction: true,
                }" :creative-effect="{
    prev: {
        shadow: false,
        translate: ['-20%', 0, -1],
    },
    next: {
        translate: ['100%', 0, 0],
    },
}" :navigation="true">
                <SwiperSlide v-for="(imageSlider, idx) in imageSliders" :key="idx">
                    <img :src="`_nuxt/assets/img/${imageSlider}`" alt="" />
                </SwiperSlide>
            </Swiper>
        </section>
        <section class="section">
            <Swiper :modules="[SwiperAutoplay, SwiperNavigation]" :slides-per-view="3" :loop="true" :navigation="true">
                <SwiperSlide v-for="(banner, idx) in banners" :key="idx" class="mx-0.5">
                    <a :href="banner.url">
                        <div class="card-container">
                            <img :src="`_nuxt/assets/img/${banner.img}`" style="width:100%" />
                            <div class="mx-4 -mt-2 pb-1 text-justify">
                                <p>{{ banner.text }}</p>
                            </div>
                        </div>
                    </a>
                </SwiperSlide>
            </Swiper>
            <div class="col-span-12 text-center my-3">
                <a href="#" class="btn btn-success btn-xl btn-round text-uppercase">See More</a>
            </div>
        </section>
        <section class="section">
            <div class="container">
                <div class="grid grid-cols-2 divide-x divide-blue-200">
                    <div class="grid grid-cols-2 divide-x divide-white">
                        <div>
                            <img src="~/assets/img/drpada-9372d.png" style="width:70%">
                        </div>
                        <div class="mx-4 text-justify">
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, itaque dignissimos minus
                                illum nostrum
                                velit sequi odio molestiae culpa fuga?</p>
                            <div class="col-span-12 text-center my-3">
                                <a href="#" class="btn btn-success btn-xl btn-round text-uppercase">Tanya Sekarang</a>
                            </div>
                        </div>
                    </div>
                    <div>
                        <div class="mx-4 text-justify">
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, itaque dignissimos minus
                                illum
                                nostrum
                                velit sequi odio molestiae culpa fuga?</p>
                            <div class="col-span-12 text-center my-3">
                                <a href="#" class="btn btn-success btn-xl btn-round text-uppercase">See More</a>
                            </div>
                        </div>
                    </div>
                </div>

            </div>
        </section>
    </div>
</template>

<script setup>
import { banners, imageSliders } from 'assets/constants';
</script>

<style scoped>
h2 {
    margin-bottom: 20px;
    font-size: 36px;
}

p {
    margin: 20px 0;
}

.card {
    /* Add shadows to create the "card" effect */
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    transition: 0.3s;
}

/* On mouse-over, add a deeper shadow */
.card:hover {
    box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}

/* Add some padding inside the card container */
.card-container {
    width: 95%;
    margin: 12px;
    background-color: #5b7cf56d;
}

.btn {
    font-size: 11px;
    padding: 8px 26px 6px;
    letter-spacing: 1.2px;
    text-transform: uppercase;
    border-radius: 2px;
    outline: none;
    -webkit-transition: 0.15s linear;
    transition: 0.15s linear;
}

.btn-round {
    border-radius: 10rem;
}

.btn-xl {
    padding: 10px 38px 10px;
    font-size: 13px;
}

.btn-success {
    color: #fff;
    background-color: #1FA345;
    border-color: #1FA345;
}

.text-uppercase {
    text-transform: uppercase !important;
}
</style>