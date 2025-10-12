<template>
    <UHeader title="Anatole" class=" shadow-2xl w-1/2 h-20 fixed top-5 left-1/2 translate-x-[-50%] rounded-full border-2" :toggle="false">
        <template #right><UColorModeSwitch /></template>
    </UHeader>

    <UContainer class=" w-full h-20" />

    <UMain>
        <UPageSection title="Anatole BROGGI" icon="i-lucide-rocket" description="Bonjour, je suis Anatole BROGGI, j’ai 15 ans et je suis développeur freelance."></UPageSection>

        <USeparator />

        <UPageSection title="Mes projets" icon="i-lucide-briefcase" description="Voici un petit aperçu de mes projets :">
            <UPageGrid>
                <UPageCard title="SchoolNet" description="Voici SchoolNet, un résau sociale pour partager des fiches de révisions." icon="i-lucide-school" class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer"></UPageCard>
                <UPageCard title="SimpleLead" description="Voici SimpleLead, un CRM ultra simple qui permet de gérer facilement votre activité." icon="i-lucide-dollar-sign" class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer"></UPageCard>
                <UPageCard title="Mon C.V" description="Voici mon C.V que j'ai créé pour mon stage de seconde dans une agence web." icon="i-lucide-globe" class=" shadow-xl hover:scale-105 hover:shadow-primary-300 transition cursor-pointer"></UPageCard>
            </UPageGrid>
        </UPageSection>
    </UMain>
</template>
