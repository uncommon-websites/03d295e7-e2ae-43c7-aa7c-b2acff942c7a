<script lang="ts">
    export let variant: 'dark' | 'light' = 'dark';
</script>

<div class="flex gap-3">
    <!-- App Store -->
    <a href="#" class="transition-opacity hover:opacity-80">
        <img 
            src="https://upload.wikimedia.org/wikipedia/commons/3/3c/Download_on_the_App_Store_Badge.svg" 
            alt="Download on the App Store" 
            class="h-10"
        />
    </a>
    <!-- Google Play -->
    <a href="#" class="transition-opacity hover:opacity-80">
        <img 
            src="https://upload.wikimedia.org/wikipedia/commons/7/78/Google_Play_Store_badge_EN.svg" 
            alt="Get it on Google Play" 
            class="h-10"
        />
    </a>
</div>
