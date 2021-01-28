<script>
    import {fade} from 'svelte/transition'
    import {t} from '../i18n'
</script>

<div class="container mt-5 py-5 d-flex flex-column justify-content-center align-items-center">
    <div class="pb-4 text-center">
        {$t('projects')}
    </div>
    <img src="images/violin.jpeg" alt="violin" in:fade={{duration:1500}}>
</div>

<style>
    .container {
        height: 100vh;
    }
    img {
        max-width: 90vw;
    }
</style>