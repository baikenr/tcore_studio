<script setup lang="ts">
import HeroSection from '@/components/hero/HeroSection.vue'
import SupportSection from '@/components/support/SupportSection.vue'
import ProjectsSection from '@/components/projects/projectsSection.vue'
import CubeSection from '@/components/cube/CubeSection.vue'
import PricingSection from '@/components/price/PricingSection.vue'
import CreatingWebsite from '@/components/aboutCreatingWebsite/creatingWebsite.vue'
import Footer from '@/components/Footer.vue'
import DiscussProject from '@/components/discussProject/discussProject.vue'
</script>

<template>
  <main>
    <HeroSection />
    <ProjectsSection />
    <CreatingWebsite/>
    <SupportSection />
    <CubeSection />
    <PricingSection />
    <DiscussProject/>
    <Footer />
  </main>
</template>
