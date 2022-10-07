<template>
    <div class="bg-light-2 pt-6 trendy">
        <div class="container">
            <div class="heading heading-flex mb-3">
                <div class="heading-left">
                    <h2 class="title">Trending Now</h2>
                </div>

                <div class="heading-right">
                    <tabs
                        class="nav-pills nav-border-anim justify-content-center"
                        :data="tabsData"
                        id="featured"
                    ></tabs>
                </div>
            </div>

            <div class="tab-content tab-content-carousel">
                <div class="tab-pane fade show active" id="featured-women">
                    <div class="swiper-carousel carousel-with-shadow swiper-1">
                        <div class="mb-0" v-swiper:swiper1="carouselSetting1">
                            <div class="swiper-wrapper">
                                <div
                                    class="swiper-slide"
                                    v-for="(product, index) in coatProducts"
                                    :key="index"
                                >
                                    <product-twelve :product="product"></product-twelve>
                                </div>
                            </div>
                        </div>
                        <div class="swiper-nav">
                            <div class="swiper-prev">
                                <i class="icon-angle-left"></i>
                            </div>
                            <div class="swiper-next">
                                <i class="icon-angle-right"></i>
                            </div>
                        </div>
                        <div class="swiper-dots d-lg-none swiper-dots-inner"></div>
                    </div>
                </div>

                <div class="tab-pane fade" id="featured-men">
                    <div class="swiper-carousel carousel-with-shadow swiper-2">
                        <div class="mb-0" v-swiper:swiper2="carouselSetting2">
                            <div class="swiper-wrapper">
                                <div
                                    class="swiper-slide"
                                    v-for="(product, index) in menProducts"
                                    :key="index"
                                >
                                    <product-twelve :product="product"></product-twelve>
                                </div>
                            </div>
                        </div>
                        <div class="swiper-dots d-lg-none swiper-dots-inner"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import Tabs from '~/components/elements/Tabs';
import ProductTwelve from '~/components/elements/products/ProductTwelve';

import { catFilter } from '~/utilities/common';
import { carouselSetting1 } from '~/utilities/carousel';

export default {
    components: {
        Tabs,
        ProductTwelve
    },
    props: {
        products: Array
    },
    data: function() {
        return {
            tabsData: [
                {
                    id: 'coat',
                    title: "コート",
                    active: true
                },
                {
                    id: 'men',
                    title: "Men's Clothing"
                }
            ],
            carouselSetting1: {
                ...carouselSetting1,
                slidesPerView: 4,
                pagination: {
                    el: '.trendy .swiper-1 .swiper-dots',
                    clickable: true
                },
                navigation: {
                    nextEl: '.trendy .swiper-1 .swiper-next',
                    prevEl: '.trendy .swiper-1 .swiper-prev'
                }
            },
            carouselSetting2: {
                ...carouselSetting1,
                slidesPerView: 4,
                pagination: {
                    el: '.trendy .swiper-2 .swiper-dots',
                    clickable: true
                }
            }
        };
    },
    computed: {
        menProducts: function() {
            return catFilter(this.products, ['men']).slice(0, 5);
        },
        coatProducts: function() {
            return catFilter(this.products, ['coat']).slice(0, 5);
        }
    }
};
</script>
