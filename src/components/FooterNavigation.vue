<template>
    <footer id="footer" class="container--wide">
        <div class="quote" cite="Kung Fu Panda, 2008">
            <blockquote>
                Yesterday is history,<br />
                tomorrow is a mystery,<br />
                but today is a gift, that is why it is called the present.
            </blockquote>

            <span>- Oogway</span>
        </div>

        <div class="flex">
            <div class="circle-group">
                <div class="circle text"></div>
                <div class="circle primary"></div>
                <div class="circle umber"></div>
                <div class="circle accent"></div>
            </div>

            <div class="links">
                <a
                    v-for="link in socialLinks"
                    :key="link.label"
                    :href="link.to"
                    target="_blank"
                    rel="noopener noreferrer"
                >
                    {{ link.label }}
                </a>
            </div>
        </div>
    </footer>
</template>

<script setup>
import { useSocialLinks } from '@/composables/useSocialLinks'

const socialLinks = useSocialLinks()
</script>

<style scoped>
footer {
    margin-top: 4em;
    margin-bottom: 2em;
}

.quote {
    color: var(--color-umber);
    border: 2px dashed var(--color-primary);
    padding: 2em;
}

blockquote {
    margin-bottom: 1rem;
}

.flex {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 1em;
}

.links {
    display: flex;
    gap: 1em;
}

.circle-group {
    display: flex;
    gap: 0.4em;
}

.circle {
    height: 1.5em;
    aspect-ratio: 1;
}

.text {
    background: var(--color-text);
}

.primary {
    background: var(--color-primary);
}

.umber {
    background: var(--color-umber);
}

.accent {
    background: var(--color-accent);
}
</style>
