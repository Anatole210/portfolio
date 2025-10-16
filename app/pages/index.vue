<template>
    <UHeader title="Anatole" class=" overflow-hidden shadow-2xl w-1/2 h-20 fixed top-5 left-1/2 translate-x-[-50%] rounded-full border-2 animate__animated animate__fadeInLeftBig " style="animation-delay: 200ms;" :toggle="false">
        <template #right><UColorModeSwitch /></template>
    </UHeader>

    <UContainer class=" w-full h-20" />

    <UMain class=" overflow-hidden">
        <UPageSection title="Anatole BROGGI" icon="i-lucide-rocket" description="Bonjour, je suis Anatole BROGGI et je suis développeur Vue.js et Nuxt en freelance." style="animation-delay: 200ms;" class=" animate__animated animate__fadeInRight"></UPageSection>

        <USeparator />

        <UPageSection title="Mes compétences" icon="i-lucide-hammer" description="Voici les pricinpales technologies que je maîtrise :" style="animation-delay: 700ms;" class=" animate__animated animate__fadeInUpBig">
            <UPageGrid>
                <UPageCard title="Javascript" icon="i-logos-javascript" description="Je miatrise javascript côté front-end et je suis entrain de l'apprendre cote backend." class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer"></UPageCard>
                <UPageCard title="Vue.js" description="Je maitrise Vue.js, ça me permet de créer des interfaces front-end réactive et personnalisé pour chaque utilisateur." class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer" icon="i-logos-vue"></UPageCard>
                <UPageCard title="Nuxt" description="Je maîtrise Nuxt et sa librairie de composants NuxtUI. Ça me permet de créer des interfaces moderne et épuré en peu de temps." class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer" icon="i-logos-nuxt-icon"></UPageCard>
            </UPageGrid>
        </UPageSection>

        <USeparator />

        <UPageSection class="timeline opacity-0 translate-x-96" title="Mes parcours" description="Voici une vue d'ensemble de mon parcours :">
            <UContainer class=" flex flex-col items-center justify-center">
                <UTimeline :items="timelineItems" :default-value="2" />
            </UContainer>
        </UPageSection>

        <USeparator />

        <UPageSection class="contact -translate-x-96 opacity-0" title="Me contacter" description="Voici mes coordonnés pour me contacter :" icon="i-lucide-user-round">
            <UPageGrid>
                <UPageCard title="Github" description="Vous pouvez cliquer pour visiter mon github." class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer" icon="i-logos-github"></UPageCard>
                <UPageCard title="Email" description="Voici mon email" class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer" icon="i-lucide-mail"></UPageCard>
                <UPageCard title="Fiverr" description="Vour pouvez cliquer pour visiter mon Fiverr" class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer" icon="i-lucide-truck"></UPageCard>
            </UPageGrid>
        </UPageSection>
    </UMain>

    <UFooter>
        <template #default>
            <div class=" flex flex-row gap-2">Made with <div class=" animate-bounce">❤️</div> by Anatole</div>
        </template>
    </UFooter>
</template>

<script setup>
import 'animate.css'
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
    gsap.to(".timeline", {
        x: 0,
        opacity: 1,
        scrollTrigger: {
            trigger: ".timeline",
            start: "top 80%",
            end: "bottom 90%",
            scrub: true,
            markers: true
        }
    })

    gsap.to(".contact", {
        x: 0,
        opacity: 1,
        scrollTrigger: {
            trigger: ".contact",
            start: "top 80%",
            end: "bottom 90%",
            scrub: true,
            markers: true
        }
    })
})

const timelineItems = ref([
  {
    date: 'Oct 2022',
    title: 'HTML, CSS',
    description: 'Apprentissage des bases du HTML et du CSS.',
    icon: 'i-simple-icons-html5'
  },
  {
    date: 'Oct 2023',
    title: 'Javascript',
    description: 'Apprentissage de JavaScript dans le but de créer des interfaces réactives.',
    icon: 'i-simple-icons-javascript'
  },
  {
    date: 'Oct 2024',
    title: 'Vue.js & Nuxt 3',
    description: 'Apprentissage de Vue.js et Nuxt 3 pour créer des applications web modernes.',
    icon: 'i-simple-icons-nuxt'
  },
  {
    date: '2025',
    title: 'Premier projet freelance',
    description: 'Créer et livrer mon premier projet en tant que développeur freelance.',
    icon: 'i-lucide-check-circle'
  }
])
</script>
