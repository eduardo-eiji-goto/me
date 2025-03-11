<template>
    <header>
        <div class="[ header__inner ] [ container--wide ]">
            <!-- Skip to Content link -->
            <a id="skip-to-content" href="#main" aria-label="Skip to Content" class="header__title">
                <span>{{ `<` }}</span
                >skip-to-content <span>{{ `/>` }}</span>
            </a>

            <!-- Home Link -->
            <a href="/me/" class="header__title">
                <span>{{ `<` }}</span
                >goto-eduardo <span>{{ `/>` }}</span>
            </a>

            <!-- Navigation -->
            <!-- Show a button on Small screens -->
            <nav v-if="isLargeScreen" class="header__nav">
                <a v-for="link in navLinks" :key="link.label" :href="link.path">
                    {{ link.label }}
                </a>
            </nav>
            <button
                v-else
                class="mobile-nav__button"
                @click="openNavigation = !openNavigation"
                aria-label="Show Mobile Navigation"
            >
                <IconMenu v-if="!openNavigation" />
                <IconX v-else />
            </button>
        </div>

        <Transition>
            <!-- Navigation for Small screens -->
            <nav v-if="openNavigation" class="header__nav--mobile">
                <a
                    @click="openNavigation = false"
                    v-for="link in navLinks"
                    :key="link.label"
                    :href="link.hash ? { path: link.path, hash: link.hash } : `${link.path}`"
                >
                    {{ link.label }}
                </a>
            </nav>
        </Transition>
    </header>
</template>

<script setup>
import { ref } from 'vue'
import { useMediaQuery } from '@vueuse/core'

import IconMenu from '@/components/icons/IconMenu.vue'
import IconX from '@/components/icons/IconX.vue'

const navLinks = [
    {
        label: 'About Me',
        path: '#about-me',
    },
    {
        label: 'Work History',
        path: '#work-history',
    },
    {
        label: 'Education',
        path: '#education',
    },
]

const isLargeScreen = useMediaQuery('(min-width: 50rem)')
const openNavigation = ref(false)
</script>

<style scoped>
header {
    position: sticky;
    top: 0;
    background-color: var(--color-base);
    z-index: 1;

    #skip-to-content {
        position: absolute;
        transform: translateY(-300%);
    }

    #skip-to-content:focus {
        transform: translateY(0);
    }

    .header__inner {
        display: flex;
        justify-content: space-between;
        padding: 1em 0;
        align-items: center;
    }

    .header__title {
        font-size: 1.2rem;
        text-decoration: none;
    }

    .header__title > span {
        color: var(--color-primary);
    }

    .header__nav > a:not(:last-child) {
        margin-right: 2em;
    }

    /* Mobile Navigation */
    .mobile-nav__button {
        height: 1.5rem;
        aspect-ratio: 1;
    }

    .header__nav--mobile {
        position: absolute;
        background: var(--color-text);
        color: var(--color-base);
        width: 100dvw;
        min-height: 100dvh;

        display: flex;
        flex-direction: column;
    }

    .header__nav--mobile > a {
        padding: 1em;
    }
}

/* Animation for mobile navigation */
.v-enter-active,
.v-leave-active {
    transition: all 0.5s ease-in-out;
}

.v-enter-from,
.v-leave-to {
    transform: translateX(100%);
}
</style>
