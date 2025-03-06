<template>
    <section class="container">
        <article>
            <h1>
                <span class="hello">Hello World!</span> <br />
                I'm
                <span class="name">Eduardo Eiji Goto</span>
            </h1>

            <p>
                Just a chill Developer from Curitiba. <br />
                Trying to make the world a better place, one
                <span class="line-through">div</span> step at a time.
            </p>

            <div class="button-group">
                <PetitPave class="petit-pave" />
                <a
                    v-for="link in socialLinks"
                    :key="link.label"
                    :href="link.to"
                    target="_blank"
                    rel="noopener noreferrer"
                    class="social-link"
                >
                    <span>{{ link.label }}</span>
                </a>
            </div>
        </article>
    </section>
</template>

<script setup>
import PetitPave from './PetitPave.vue'

import { useSocialLinks } from '@/composables/useSocialLinks'

const socialLinks = useSocialLinks()
</script>

<style scoped>
section {
    margin-top: 8rem;
    display: grid;
    gap: 1rem;
    grid-template-columns: auto auto;

    position: relative;

    .hello {
        color: var(--color-umber);
    }

    .name {
        color: var(--color-primary);
        font-weight: bolder;
    }

    p {
        font-size: 1.4rem;
        max-width: 40ch;
        margin-bottom: 3rem;
    }

    .button-group {
        display: flex;
        gap: 1rem;
        margin-bottom: 1rem;
        align-items: center;
    }

    .social-link {
        padding: 0.5rem 2rem;
        border: 2px dashed var(--color-primary);
        text-decoration: none;
        background-color: var(--color-base);
    }

    .social-link:focus {
        border: none;
    }

    .social-link:focus,
    .social-link:hover {
        background-color: var(--color-accent);
    }

    .me-picture {
        width: 18rem;
        aspect-ratio: 1;
        object-fit: cover;
        border-radius: 100%;
    }

    @media screen and (max-width: 50rem) {
        margin-top: 1rem;
        display: flex;
        flex-direction: column-reverse;
        align-items: center;
        text-align: center;

        article {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
    }
}

.petit-pave {
    width: 5em;
    height: 5em;

    fill: var(--color-primary);
}

@media screen and (min-width: 50rem) {
    .petit-pave {
        position: absolute;
        z-index: -1;
        right: 0;
        bottom: 0;
        transform: translate(25%, 15%);

        width: 20em;
        height: 20em;

        fill: var(--color-accent);
        opacity: 0.5;
    }
}

.line-through {
    text-decoration: 2px line-through;
}
</style>
