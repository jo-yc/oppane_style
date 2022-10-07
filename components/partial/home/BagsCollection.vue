<template>
    <div class="container featured bags mt-4 pb-2">
        <div class="heading heading-flex mb-3">
            <div class="heading-left">
                <h2 class="title">Bags & Accessories</h2>
            </div>

            <div class="heading-right">
                <tabs
                    class="nav-pills nav-border-anim justify-content-center"
                    :data="tabsData"
                    id="bags"
                ></tabs>
            </div>
        </div>

        <div class="row">
            <div class="col-lg-3">
                <div class="banner banner-overlay product-banner">
                    <a href="#">
                        <img
                            v-lazy="'./images/home/banners/banner-6.jpg'"
                            width="277"
                            height="530"
                            alt="banner"
                        />
                    </a>
                    <div class="banner-content">
                        <div class="banner-top">
                            <div class="banner-title text-white text-center">
                                <i class="la la-star-o"></i>
                                <h3 class="text-white">
                                    Our Experts
                                    <br />Recommend
                                </h3>
                            </div>
                        </div>
                        <div class="banner-bottom">
                            <div class="product-cat">
                                <h4 class="text-white">Sale</h4>
                            </div>
                            <div class="product-price">
                                <h4 class="text-white">$29.99</h4>
                            </div>
                            <div class="product-txt">
                                <p class="text-white">Wedge-heel sandals</p>
                            </div>
                            <nuxt-link
                                to="/shop/sidebar/list"
                                class="btn btn-outline-white banner-link"
                            >Shop Now</nuxt-link>
                        </div>
                    </div>
                </div>
            </div>

            <div class="col-lg-9">
                <div class="tab-content tab-content-carousel">
                    <div class="tab-pane fade show active" id="bags-women">
                        <div class="swiper-carousel carousel-with-shadow swiper-1">
                            <div class="mb-0" v-swiper:swiper1="carouselSetting1">
                                <div class="swiper-wrapper">
                                    <div
                                        class="swiper-slide"
                                        v-for="(product, index) in womenProducts"
                                        :key="index"
                                    >
                                        <product-twelve :product="product"></product-twelve>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="tab-pane fade" id="bags-men">
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
                        </div>
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
                    id: 'women',
                    title: "Women's",
                    active: true
                },
                {
                    id: 'men',
                    title: "Men's"
                }
            ],
            carouselSetting1: {
                ...carouselSetting1,
                slidesPerView: 3
            },
            carouselSetting2: {
                ...carouselSetting1,
                slidesPerView: 3
            }
        };
    },
    computed: {
        menProducts: function() {
            return catFilter(this.products, ['men']);
        },
        womenProducts: function() {
            return catFilter(this.products, ['women']).slice(0, 3);
        }
    }
};
</script>
