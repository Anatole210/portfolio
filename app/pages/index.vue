<template>
    <UHeader title="Anatole" class=" overflow-hidden shadow-2xl w-1/2 h-20 fixed top-5 left-1/2 translate-x-[-50%] rounded-full border-2 animate__animated animate__fadeInLeftBig " style="animation-delay: 200ms;" :toggle="false">
        <template #right><UColorModeSwitch /></template>
    </UHeader>

    <UContainer class=" w-full h-20" />

    <UMain class=" overflow-hidden">
        <UPageSection title="Anatole BROGGI" icon="i-lucide-rocket" description="Bonjour, je suis Anatole BROGGI, j’ai 15 ans et je suis développeur freelance." style="animation-delay: 200ms;" class=" animate__animated animate__fadeInRight"></UPageSection>

        <USeparator />

        <UPageSection title="Mes projets" icon="i-lucide-briefcase" description="Voici un petit aperçu de mes projets :" style="animation-delay: 700ms;" class=" animate__animated animate__fadeInUpBig">
            <UPageGrid>
                <UPageCard title="SchoolNet" description="Voici SchoolNet, un résau sociale pour partager des fiches de révisions." icon="i-lucide-school" class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer"></UPageCard>
                <UPageCard title="SimpleLead" description="Voici SimpleLead, un CRM ultra simple qui permet de gérer facilement votre activité." icon="i-lucide-dollar-sign" class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer"></UPageCard>
                <UPageCard title="Mon C.V" description="Voici mon C.V que j'ai créé pour mon stage de seconde dans une agence web." icon="i-lucide-globe" class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer"></UPageCard>
            </UPageGrid>
        </UPageSection>

        <USeparator />

        <UPageSection title="Mes compétences" icon="i-lucide-hammer" description="Voici les pricinpales technologies que je maîtrise :">
            <UPageGrid>
                <UPageCard title="Javascript" icon="i-logos-javascript" description="Je miatrise javascript côté front-end et je suis entrain de l'apprendre cote backend." class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer"></UPageCard>
                <UPageCard title="Vue.js" description="Je maitrise Vue.js, ça me permet de créer des interfaces front-end réactive et personnalisé pour chaque utilisateur." class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer" icon="i-logos-vue"></UPageCard>
                <UPageCard title="Nuxt" description="Je maîtrise Nuxt et sa librairie de composants NuxtUI. Ça me permet de créer des interfaces moderne et épuré en peu de temps." class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer" icon="i-logos-nuxt-icon"></UPageCard>
            </UPageGrid>
        </UPageSection>

        <USeparator />

        <UPageSection title="Mes parcours" description="Voici une vue d'ensemble de mon parcours :">
            <UContainer class=" flex flex-col items-center justify-center">
                <UTimeline :items="timelineItems" :default-value="2" />
            </UContainer>
        </UPageSection>

        <USeparator />

        <UPageSection title="Me contacter" description="Voici mes coordonnés pour me contacter :" icon="i-lucide-user-round">
            <UPageGrid>
                <UPageCard title="Github" description="Vous pouvez cliquer pour visiter mon github." class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer" icon="i-logos-github"></UPageCard>
                <UPageCard title="Email" description="Voici mon email" class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer" icon="i-lucide-mail"></UPageCard>
                <UPageCard title="Fiverr" description="Vour pouvez cliquer pour visiter mon Fiverr" class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer" icon="i-lucide-truck"></UPageCard>
            </UPageGrid>
            <UForm>
                <h2>Envoyer un message</h2>
                <UFormField label="Email" required><UInput placeholder="Votre email..." type="email" icon="i-lucide-mail" required></UInput></UFormField>
                <UFormField label="Titre" required><UInput placeholder="Titre du message..." icon="i-lucide-text" required></UInput></UFormField>
                <UFormField label="Message" required><UTextarea icon="i-lucide-text" placeholder="Votre message..." required autoresize></UTextarea></UFormField>
                <UButton label="Envoyer votre message" type="submit" icon="i-lucide-send" />
            </UForm>
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

const timelineItems = ref([
  {
    date: '??/??/????',
    title: 'HTML, CSS',
    description: 'Apprentissage des bases du HTML et du CSS.',
    icon: 'i-simple-icons-html5'
  },
  {
    date: '??/??/????',
    title: 'Javascript',
    description: 'Apprentissage de jaavscript dans le but de créer des interfaces réactives.',
    icon: 'i-simple-icons-javascript'
  },
  {
    date: 'Mar 29 2025',
    title: 'Development Sprint',
    description: 'Frontend and backend development. Implemented core features and integrated with APIs.',
    icon: 'i-lucide-code'
  },
  {
    date: 'Apr 5 2025',
    title: 'Testing & Deployment',
    description: 'QA testing and performance optimization. Deployed the application to production.',
    icon: 'i-lucide-check-circle'
  }
])
</script>
