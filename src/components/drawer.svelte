<script lang="ts">
    import { fly } from 'svelte/transition';
    import FilledButton from '@components/button-filled.svelte'
    import TextButton from '@components/button-text.svelte'

    const links = [
        "Features",
        "Pricing",
        "Resources",
    ]
</script>

<template>
    <aside class="absolute bottom-0 left-1/2 -translate-x-1/2 translate-y-full w-full max-w-lg h-auto px-6 pt-4 lg:hidden" transition:fly="{{ y: -24, duration: 150 }}">
        <div class="w-full h-auto bg-dark-violet rounded-lg shadow-xl px-6 py-10">
            <nav class="flex flex-col justify-start items-center space-y-4 w-full h-auto">
                {#each links as link}
                    <a class="text-lg font-bold text-white transition-colors hover:text-cyan" href="/">{ link }</a>
                {/each}
            </nav>
            <div class="w-full h-px bg-white opacity-10 my-8"></div>
            <div class="flex flex-col justify-start items-stretch w-full h-auto space-y-4">
                <TextButton size="lg" label="Login" onDark />
                <FilledButton size="md" label="Sign Up" rounded />
            </div>
        </div>
    </aside>
</template>