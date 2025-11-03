<script setup lang="ts">
    const props = defineProps<{
        items: { label: string; href?: string }[]
        arrowTo?: string
        stripeWidths?: [number, number, number]
    }>();

    import { useScrollTo } from '@/composables/useScrollTo';
    const { to } = useScrollTo();

    const widths = props.stripeWidths ?? [154, 152, 152];
</script>

<template>
    <nav
        class="hero__nav" :style="{ gridTemplateColumns: `${widths[0]}px ${widths[1]}px ${widths[2]}px 70px` }"aria-label="Hero menu">
        <a v-for="(it, i) in items" :key="i" class="nav-link" :href="it.href || '#'" @click.prevent> {{ it.label }}</a>
        <button class="arrow" aria-label="scroll down" @click="arrowTo && to(arrowTo)">⌄</button>
    </nav>
</template>

<style scoped>
    .hero__nav{
        position:absolute; right:0; bottom:0; z-index:6;
        height:80px; display:grid;
    }
    .nav-link{
        display:flex; align-items:center; justify-content:center;
        color:#fff; font-size:20px; font-weight:700; text-decoration:none;
        background:transparent; backdrop-filter:none;
        transition:opacity .25s, transform .25s;
        pointer-events:auto;
    }
    .nav-link:hover{ opacity:.92; transform:translateY(-2px); }

    .arrow{
        display:flex; align-items:center; justify-content:center;
        width:100%; height:100%;
        background:transparent; border:0; color:#fff; font-size:36px; cursor:pointer;
        transition:transform .25s, opacity .25s;
    }
    .arrow:hover{ transform:translateY(3px); opacity:.95; }
</style>