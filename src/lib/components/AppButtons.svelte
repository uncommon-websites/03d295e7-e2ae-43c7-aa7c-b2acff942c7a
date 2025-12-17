<script lang="ts">
    export let variant: 'dark' | 'light' = 'dark';
</script>

<div class="flex flex-wrap items-center gap-4">
    <!-- App Store -->
    <a
        href="#"
        class="inline-block transition-all duration-200 hover:opacity-80 hover:scale-[1.02] active:scale-[0.98]"
    >
        <img
            src="/app-store-badge.svg"
            alt="Download on the App Store"
            class="h-12"
        />
    </a>

    <!-- Google Play -->
    <a
        href="#"
        class="inline-block transition-all duration-200 hover:opacity-80 hover:scale-[1.02] active:scale-[0.98]"
    >
        <img
            src="/google-play-badge.svg"
            alt="Get it on Google Play"
            class="h-12"
        />
    </a>
</div>
