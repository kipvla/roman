<script>
	import Navbar from './components/Navbar.svelte'
	import Hero from './components/Hero.svelte'
	import { dictionary, locale } from 'svelte-i18n';

	dictionary.set({
        en: {
            app: {
                title: 'Filmic',
                subtitle: 'A curated collection of eighties movies',
            },
        },
        ar: {
            app: {
                title: 'فيلميك',
                subtitle: 'مجموعة أفلام مختارة من الثمنينات',
            },
        },
    });
    locale.set('en');
</script>

<main>
	<Navbar />
	<Hero />
</main>

<style>
	
</style>