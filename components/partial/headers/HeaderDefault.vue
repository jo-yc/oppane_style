<template>
    <header class="header header-6">
        <div class="header-top">
            <div :class="isFullwidth ? 'container-fluid' : 'container'">
                <div class="header-left">
                    <ul class="top-menu top-link-menu d-none d-md-block">
                        <li>
                            <a href="#">Links</a>
                            <ul>
                                <li>
                                    <a href="javascript:;">
                                        <i class="icon-phone"></i>Call: +0123 456 789
                                    </a>
                                </li>
                            </ul>
                        </li>
                    </ul>
                </div>

                <div class="header-right">
                    <div class="social-icons social-icons-color">
                        <a
                            href="https://www.facebook.com"
                            class="social-icon social-facebook"
                            rel="noopener noreferrer"
                            title="Facebook"
                            target="_blank"
                        >
                            <i class="icon-facebook-f"></i>
                        </a>
                        <a
                            href="https://twitter.com"
                            class="social-icon social-twitter"
                            rel="noopener noreferrer"
                            title="Twitter"
                            target="_blank"
                        >
                            <i class="icon-twitter"></i>
                        </a>
                        <a
                            href="https://pinterest.com"
                            class="social-icon social-pinterest"
                            rel="noopener noreferrer"
                            title="Pinterest"
                            target="_blank"
                        >
                            <i class="icon-pinterest-p"></i>
                        </a>
                        <a
                            href="https://instagram.com"
                            class="social-icon social-instagram"
                            rel="noopener noreferrer"
                            title="Instagram"
                            target="_blank"
                        >
                            <i class="icon-instagram"></i>
                        </a>
                    </div>
                    <ul class="top-menu top-link-menu">
                        <li>
                            <a href="javascript:;">Links</a>
                            <ul>
                                <li>
                                    <a href="javascript:;" @click.prevent="openSignInModal">
                                        <i class="icon-user"></i>Login
                                    </a>
                                </li>
                            </ul>
                        </li>
                    </ul>
                    <div class="header-dropdown">
                        <a href="javascript:;">USD</a>
                        <div class="header-menu">
                            <ul>
                                <li>
                                    <a href="javascript:;">Eur</a>
                                </li>
                                <li>
                                    <a href="javascript:;">Usd</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                    <div class="header-dropdown">
                        <a href="javascript:;">Eng</a>
                        <div class="header-menu">
                            <ul>
                                <li>
                                    <a href="javascript:;">English</a>
                                </li>
                                <li>
                                    <a href="javascript:;">French</a>
                                </li>
                                <li>
                                    <a href="javascript:;">Spanish</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="header-middle">
            <div :class="isFullwidth ? 'container-fluid' : 'container'">
                <div class="header-left">
                    <header-search></header-search>
                </div>

                <div class="header-center">
                    <nuxt-link to="/" class="logo">
                        <img
                            v-lazy="'./images/home/logo.png'"
                            class="bg-transparent"
                            alt="Molla Logo"
                            width="82"
                            height="20"
                        />
                    </nuxt-link>
                </div>

                <div class="header-right">
                    <wishlist-menu></wishlist-menu>

                    <cart-menu></cart-menu>
                </div>
            </div>
        </div>

        <sticky-header>
            <div class="header-bottom sticky-header">
                <div :class="isFullwidth ? 'container-fluid' : 'container'">
                    <div class="header-left">
                        <main-menu></main-menu>

                        <button class="mobile-menu-toggler" @click="openMobileMenu">
                            <span class="sr-only">Toggle mobile menu</span>
                            <i class="icon-bars"></i>
                        </button>
                    </div>

                    <div class="header-right overflow-hidden">
                        <i class="la la-lightbulb-o"></i>
                        <p class="font-weight-semibold">Clearance Up to 30% Off</p>
                    </div>
                </div>
            </div>
        </sticky-header>
    </header>
</template>

<script>
import CartMenu from '~/components/partial/headers/shared/CartMenu';
import WishlistMenu from '~/components/partial/headers/shared/WishlistMenu';
import MainMenu from '~/components/partial/headers/shared/MainMenu';
import HeaderSearch from '~/components/partial/headers/shared/HeaderSearch';
import StickyHeader from '~/components/elements/StickyHeader';

export default {
    components: {
        CartMenu,
        WishlistMenu,
        MainMenu,
        HeaderSearch,
        StickyHeader
    },
    computed: {
        isFullwidth: function() {
            return this.$route.path.includes('fullwidth');
        }
    },
    methods: {
        openSignInModal: function() {
            this.$modal.show(
                () => import('~/components/elements/modals/SignInModal'),
                {},
                { width: '575', height: 'auto', adaptive: true }
            );
        },
        openMobileMenu: function() {
            document.querySelector('body').classList.add('mmenu-active');
        }
    }
};
</script>