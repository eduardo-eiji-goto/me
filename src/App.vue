<template>
    <HeaderNavigation />

    <main id="main">
        <p v-for="i in [1, 2, 3, 4, 5, 5, 6, 7, 8]" class="container">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit quisquam nesciunt
            voluptates mollitia corrupti ab hic ducimus fugiat! Aliquam in veniam dolore
            reprehenderit quod consectetur eveniet libero corrupti accusantium ea?
        </p>

        <p class="container--wide">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Recusandae quaerat ratione
            praesentium error, reprehenderit aliquam excepturi incidunt dignissimos neque aut,
            assumenda quod. Tempore quos sed, ea nobis officia saepe minus?
        </p>
    </main>

    <FooterNavigation />
</template>

<script setup>
import HeaderNavigation from './components/HeaderNavigation.vue'
import FooterNavigation from './components/FooterNavigation.vue'
</script>

<style scoped></style>
