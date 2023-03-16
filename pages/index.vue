<template>
    <div>
        <section class="section swiper-container">
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
        </section>
        <section class="section">
            <Swiper
            :modules="[SwiperAutoplay, SwiperNavigation]"
                :slides-per-view="3"
                :loop="true"
                :autoplay="{
                    delay: 8000,
                    disableOnInteraction: true,
                }"
                :navigation="true"
            >
                <SwiperSlide>
                    <div class="card">
                        <img src="~/assets/img/gasbw.png" style="width:100%">
                        <div class="card-container">
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, itaque dignissimos minus illum nostrum
                                velit sequi odio molestiae culpa fuga?</p>
                        </div>
                    </div>
                </SwiperSlide>
                <SwiperSlide>
                    <div class="card">
                        <img src="~/assets/img/obgynbwop.png" style="width:100%">
                        <div class="card-container">
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, itaque dignissimos minus illum nostrum
                                velit sequi odio molestiae culpa fuga?</p>
                        </div>
                    </div>
                </SwiperSlide>
                <SwiperSlide>
                    <div class="card">
                        <img src="~/assets/img/oncologybwop.png" style="width:100%">
                        <div class="card-container">
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, itaque dignissimos minus illum nostrum
                                velit sequi odio molestiae culpa fuga?</p>
                        </div>
                    </div>
                </SwiperSlide>
                <SwiperSlide>
                    <div class="card">
                        <img src="~/assets/img/pediatricbwop-eb05d.png" style="width:100%">
                        <div class="card-container">
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, itaque dignissimos minus illum nostrum
                                velit sequi odio molestiae culpa fuga?</p>
                        </div>
                    </div>
                </SwiperSlide>
                <SwiperSlide>
                    <div class="card">
                        <img src="~/assets/img/pulmonologistbwop.png" style="width:100%">
                        <div class="card-container">
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, itaque dignissimos minus illum nostrum
                                velit sequi odio molestiae culpa fuga?</p>
                        </div>
                    </div>
                </SwiperSlide>
                <SwiperSlide>
                    <div class="card">
                        <img src="~/assets/img/spinebw.png" style="width:100%">
                        <div class="card-container">
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, itaque dignissimos minus illum nostrum
                                velit sequi odio molestiae culpa fuga?</p>
                        </div>
                    </div>
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
                        <div>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, itaque dignissimos minus illum nostrum
                                velit sequi odio molestiae culpa fuga?</p>
                            <div class="col-span-12 text-center my-3">
                                <a href="#" class="btn btn-success btn-xl btn-round text-uppercase">Tanya Sekarang</a>
                            </div>
                        </div>
                        
                    </div>
                    <div>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis, itaque dignissimos minus illum nostrum
                            velit sequi odio molestiae culpa fuga?</p>
                        <div class="col-span-12 text-center my-3">
                            <a href="#" class="btn btn-success btn-xl btn-round text-uppercase">See More</a>
                        </div>
                    </div>
                </div>
                
            </div>
        </section>
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

.section {
    margin-bottom: 5%;
}

.card {
  /* Add shadows to create the "card" effect */
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
}

/* On mouse-over, add a deeper shadow */
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

/* Add some padding inside the card container */
.card-container {
  padding: 2px 16px;
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