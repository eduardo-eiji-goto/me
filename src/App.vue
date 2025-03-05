<template>
    <HeaderNavigation />

    <main id="main">
        <SectionIntroduction />

        <SectionAboutMe />

        <SectionWorkHistory />

        <SectionEducation />
    </main>

    <FooterNavigation />
</template>

<script setup>
import HeaderNavigation from './components/HeaderNavigation.vue'
import FooterNavigation from './components/FooterNavigation.vue'

import SectionIntroduction from './components/SectionIntroduction.vue'
import SectionAboutMe from './components/SectionAboutMe.vue'
import SectionWorkHistory from './components/SectionWorkHistory.vue'
import SectionEducation from './components/SectionEducation.vue'
</script>

<style scoped></style>
