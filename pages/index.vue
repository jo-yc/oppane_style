<template>
    <div class="main home-page">
        <div class="intro-section">
            <div class="intro-section-slider">
                <div class="container">
                    <div class="intro-slider-container slider-container-ratio mb-0">
                        <div class="swiper-carousel intro-slider swiper-1">
                            <div v-swiper:swiper1="carouselSetting1">
                                <div class="swiper-wrapper">
                                    <div class="swiper-slide">
                                        <div class="intro-slide">
                                            <figure class="slide-image mb-0">
                                                <picture>
                                                    <source
                                                        media="(max-width: 480px)"
                                                        srcset="~/static/images/home/sliders/slide-1-480w.jpg"
                                                    />
                                                    <img
                                                        src="~/static/images/home/sliders/slide-1.jpg"
                                                        alt="Image Desc"
                                                    />
                                                </picture>
                                            </figure>

                                            <div class="intro-content">
                                                <h3 class="intro-subtitle">New Collection</h3>

                                                <h1 class="intro-title text-white">
                                                    Women’s
                                                    <br />Sportswear & Joggers
                                                </h1>

                                                <div class="intro-text text-white">2021</div>

                                                <nuxt-link
                                                    to="/shop/sidebar/list"
                                                    class="btn btn-primary"
                                                >
                                                    <span>DISCOVER NOW</span>
                                                </nuxt-link>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="swiper-slide">
                                        <div class="intro-slide">
                                            <figure class="slide-image mb-0">
                                                <picture>
                                                    <source
                                                        media="(max-width: 480px)"
                                                        srcset="~/static/images/home/sliders/slide-2-480w.jpg"
                                                    />
                                                    <img
                                                        src="~/static/images/home/sliders/slide-2.jpg"
                                                        alt="Image Desc"
                                                    />
                                                </picture>
                                            </figure>

                                            <div class="intro-content">
                                                <h3 class="intro-subtitle">New Collection</h3>

                                                <h1 class="intro-title text-white">
                                                    Men’s
                                                    <br />Coats & Jackets
                                                </h1>

                                                <nuxt-link
                                                    to="/shop/sidebar/list"
                                                    class="btn btn-primary"
                                                >
                                                    <span>DISCOVER NOW</span>
                                                </nuxt-link>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="swiper-slide">
                                        <div class="intro-slide">
                                            <figure class="slide-image mb-0">
                                                <picture>
                                                    <source
                                                        media="(max-width: 480px)"
                                                        srcset="~/static/images/home/sliders/slide-3-480w.jpg"
                                                    />
                                                    <img
                                                        src="~/static/images/home/sliders/slide-3.jpg"
                                                        alt="Image Desc"
                                                    />
                                                </picture>
                                            </figure>

                                            <div class="intro-content">
                                                <h3 class="intro-subtitle">Deals and Promotions</h3>

                                                <h1
                                                    class="intro-title text-white"
                                                >Sneakers & Athletic Shoes</h1>

                                                <div class="intro-text text-white">from $9.99</div>

                                                <nuxt-link
                                                    to="/shop/sidebar/list"
                                                    class="btn btn-primary"
                                                >
                                                    <span>SHOP NOW</span>
                                                </nuxt-link>
                                            </div>
                                        </div>
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
                            <div class="swiper-dots swiper-dots-inner"></div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="icon-boxes-container pt-0 pb-0">
                <div class="container">
                    <div class="swiper-carousel">
                        <div v-swiper:swiper3="carouselSetting3">
                            <div class="swiper-wrapper">
                                <div class="swiper-slide">
                                    <div class="icon-box icon-box-side">
                                        <span class="icon-box-icon">
                                            <i class="icon-rocket"></i>
                                        </span>

                                        <div class="icon-box-content">
                                            <h3 class="icon-box-title">Free Shipping</h3>

                                            <p>Orders $50 or more</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="swiper-slide">
                                    <div class="icon-box icon-box-side">
                                        <span class="icon-box-icon">
                                            <i class="icon-rotate-left"></i>
                                        </span>

                                        <div class="icon-box-content">
                                            <h3 class="icon-box-title">Free Returns</h3>

                                            <p>Within 30 days</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="swiper-slide">
                                    <div class="icon-box icon-box-side">
                                        <span class="icon-box-icon">
                                            <i class="icon-info-circle"></i>
                                        </span>

                                        <div class="icon-box-content">
                                            <h3 class="icon-box-title">Get 20% Off 1 Item</h3>

                                            <p>When you sign up</p>
                                        </div>
                                    </div>
                                </div>
                                <div class="swiper-slide">
                                    <div class="icon-box icon-box-side">
                                        <span class="icon-box-icon">
                                            <i class="icon-life-ring"></i>
                                        </span>

                                        <div class="icon-box-content">
                                            <h3 class="icon-box-title">We Support</h3>

                                            <p>24/7 amazing services</p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="pt-3 pb-3">
            <div class="container">
                <div class="banner-group">
                    <div class="row">
                        <div class="col-sm-6 col-lg-4">
                            <div class="banner banner-overlay banner-lg">
                                <nuxt-link to="/shop/sidebar/3cols">
                                    <img
                                        v-lazy="'./images/home/banners/banner-1.jpg'"
                                        width="376"
                                        height="500"
                                        alt="Banner"
                                    />
                                </nuxt-link>

                                <div class="banner-content banner-content-bottom">
                                    <h4 class="banner-subtitle text-white">
                                        <a href="#">Clearance</a>
                                    </h4>

                                    <h3 class="banner-title text-white">
                                        <a href="#">Waterproof</a>
                                    </h3>

                                    <div class="banner-text text-white">
                                        <a href="#">from $19.00</a>
                                    </div>

                                    <nuxt-link
                                        to="/shop/sidebar/list"
                                        class="btn btn-outline-white banner-link"
                                    >Discover Now</nuxt-link>
                                </div>
                            </div>
                        </div>

                        <div class="col-sm-6 col-lg-4 order-lg-last">
                            <div class="banner banner-overlay banner-lg">
                                <nuxt-link to="/shop/sidebar/3cols">
                                    <img
                                        v-lazy="'./images/home/banners/banner-4.jpg'"
                                        width="376"
                                        height="500"
                                        alt="Banner"
                                    />
                                </nuxt-link>

                                <div class="banner-content banner-content-top">
                                    <h4 class="banner-subtitle text-white">
                                        <a href="#">On Sale</a>
                                    </h4>

                                    <h3 class="banner-title text-white">
                                        <a href="#">
                                            Women's
                                            <br />Sportswear
                                        </a>
                                    </h3>

                                    <div class="banner-text text-white">
                                        <a href="#">from $39.00</a>
                                    </div>

                                    <nuxt-link
                                        to="/shop/sidebar/list"
                                        class="btn btn-outline-white banner-link"
                                    >Discover Now</nuxt-link>
                                </div>
                            </div>
                        </div>

                        <div class="col-12 col-lg-4">
                            <div class="row">
                                <div class="col-sm-6 col-lg-12">
                                    <div class="banner banner-overlay">
                                        <nuxt-link to="/shop/sidebar/3cols">
                                            <img
                                                v-lazy="'./images/home/banners/banner-2.jpg'"
                                                width="376"
                                                height="240"
                                                alt="Banner"
                                            />
                                        </nuxt-link>

                                        <div class="banner-content">
                                            <h4 class="banner-subtitle text-white">
                                                <a href="#">New Arrivals</a>
                                            </h4>

                                            <h3 class="banner-title text-white">
                                                <a href="#">
                                                    Accessories
                                                    <br />and Shoes
                                                </a>
                                            </h3>

                                            <nuxt-link
                                                to="/shop/sidebar/list"
                                                class="btn btn-outline-white banner-link"
                                            >Shop Now</nuxt-link>
                                        </div>
                                    </div>
                                </div>

                                <div class="col-sm-6 col-lg-12">
                                    <div class="banner banner-overlay">
                                        <nuxt-link to="/shop/sidebar/3cols">
                                            <img
                                                v-lazy="'./images/home/banners/banner-3.jpg'"
                                                width="376"
                                                height="240"
                                                alt="Banner"
                                            />
                                        </nuxt-link>

                                        <div class="banner-content">
                                            <h4 class="banner-subtitle text-white">
                                                <a href="#">New Arrivals</a>
                                            </h4>

                                            <h3 class="banner-title text-white">
                                                <a href="#">Spring 2021</a>
                                            </h3>

                                            <nuxt-link
                                                to="/shop/sidebar/list"
                                                class="btn btn-outline-white banner-link"
                                            >Shop Now</nuxt-link>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- <div class="swiper-carousel brands-border swiper-2">
                    <div v-swiper:swiper2="carouselSetting2">
                        <div class="swiper-wrapper">
                            <div
                                class="swiper-slide"
                                v-for="(brand, index) in homeData.brands"
                                :key="index"
                            >
                                <a href="#" class="brand">
                                    <img
                                        v-lazy="brand.image"
                                        class="bg-white"
                                        alt="Brand"
                                        :width="brand.width"
                                        :height="brand.height"
                                    />
                                </a>
                            </div>
                        </div>
                    </div>
                </div> -->
            </div>
        </div>

        <trendy-collection :products="products" v-if="loaded"></trendy-collection>

        <footwear-collection :products="products" v-if="loaded"></footwear-collection>
        <div class="container">
            <hr class="mt-3 mb-4" />
        </div>

        <bags-collection :products="products" v-if="loaded"></bags-collection>

        <div class="container">
            <hr class="mt-3 mt-xl-1 mb-0" />
        </div>

        <div class="cta pt-4 pt-lg-6 pb-5 pb-lg-7 mb-0">
            <div class="container">
                <div class="row justify-content-center">
                    <div class="col-sm-10 col-md-8 col-lg-6">
                        <div class="cta-heading text-center">
                            <h3 class="cta-title">Sign Up for updates from Molla</h3>

                            <p class="cta-desc">
                                and receive
                                <span class="font-weight-normal">$20 coupon</span> for first shopping
                            </p>
                        </div>

                        <form action="#">
                            <div class="input-group">
                                <input
                                    type="email"
                                    class="form-control"
                                    placeholder="Enter your Email Address"
                                    aria-label="Email Adress"
                                    required
                                />
                                <div class="input-group-append">
                                    <button class="btn btn-primary" type="submit" title="Sing up">
                                        <i class="icon-long-arrow-right"></i>
                                    </button>
                                </div>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>

        <div class="swiper-carousel brands-border swiper-4">
            <div v-swiper:swiper4="carouselSetting4">
                <div class="swiper-wrapper">
                    <div
                        class="swiper-slide"
                        v-for="(instagram, index) in homeData.instagrams"
                        :key="index"
                    >
                        <div class="instagram-feed bg-white h-auto mb-0">
                            <img
                                v-lazy="instagram.img"
                                class="bg-white"
                                alt="Instagram"
                                width="320"
                                height="320"
                            />

                            <div class="instagram-feed-content">
                                <a href="#">
                                    <i class="icon-heart-o"></i>
                                    {{ instagram.likes }}
                                </a>
                                <a href="#">
                                    <i class="icon-comments"></i>
                                    {{ instagram.comments }}
                                </a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { mapGetters } from 'vuex';

import TrendyCollection from '~/components/partial/home/TrendyCollection';
import FootwearCollection from '~/components/partial/home/FootwearCollection';
import BagsCollection from '~/components/partial/home/BagsCollection';
import NewsletterModal from '~/components/elements/modals/NewsletterModal';

import Repository, { baseUrl } from '~/repositories/repository.js';
import { attrFilter } from '~/utilities/common';
import {
    carouselSettingSingle,
    carouselSettingDefault
} from '~/utilities/carousel';
import { homeData } from '~/utilities/data';

export default {
    components: {
        FootwearCollection,
        TrendyCollection,
        BagsCollection
    },
    data: function() {
        return {
            loaded: false,
            products: [],
            carouselSetting1: {
                ...carouselSettingSingle,
                loop: true,
                navigation: {
                    nextEl: '.intro-slider .swiper-next',
                    prevEl: '.intro-slider .swiper-prev'
                },
                pagination: {
                    el: '.intro-slider .swiper-dots',
                    clickable: true
                }
            },
            carouselSetting2: {
                ...carouselSettingDefault,
                slidesPerView: 6,
                spaceBetween: 20,
                breakpoints: {
                    992: {
                        slidesPerView: 5
                    },
                    768: {
                        slidesPerView: 4
                    },
                    576: {
                        slidesPerView: 3
                    },
                    480: {
                        slidesPerView: 2
                    }
                }
            },
            carouselSetting3: {
                ...carouselSettingDefault,
                slidesPerView: 4,
                spaceBetween: 20,
                breakpoints: {
                    992: {
                        slidesPerView: 3
                    },
                    768: {
                        slidesPerView: 2
                    },
                    576: {
                        slidesPerView: 2
                    },
                    480: {
                        slidesPerView: 1
                    }
                }
            },
            carouselSetting4: {
                ...carouselSettingDefault,
                slidesPerView: 6,
                spaceBetween: 0,
                breakpoints: {
                    992: {
                        slidesPerView: 5
                    },
                    768: {
                        slidesPerView: 4
                    },
                    576: {
                        slidesPerView: 3
                    },
                    480: {
                        slidesPerView: 2
                    }
                }
            },
            homeData: homeData
        };
    },
    computed: {
        ...mapGetters('demo', ['newsletterShow'])
    },
    created: function() {
        this.getProducts();
    },
    mounted: function() {
        if (this.newsletterShow) {
            setTimeout(() => {
                if (this.$route.path == '/' && this.newsletterShow) {
                    this.$modal.show(
                        NewsletterModal,
                        {},
                        { width: '970', height: 'auto', adaptive: true }
                    );
                }
            }, 8000);
        }
    },
    methods: {
        getProducts: async function() {
            this.loaded = false;
            await Repository.get(`${baseUrl}/oppa_style`)
                .then(response => {
                    this.products = response.data.products;
                    this.loaded = true;
                })
                .catch(error => ({ error: JSON.stringify(error) }));
        }
    }
};
</script>
