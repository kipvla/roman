<script>
	import Navbar from './components/Navbar.svelte'
	import Footer from './components/Footer.svelte'
    import {Router,Route} from 'svelte-routing'
    import Home from './pages/Home.svelte'
    import About from './pages/About.svelte'
    import Projects from './pages/Projects.svelte'
    import Media from './pages/Media.svelte'
    import Teacher from './pages/Teacher.svelte'
    import Contact from './pages/Contact.svelte'
</script>

<main>
	<Router>
        <Navbar />
        <Route path="/" component={Home}/>
        <Route path="/about" component={About}/>
        <Route path="/projects" component={Projects}/>
        <Route path="/media" component={Media}/>
        <Route path="/teacher" component={Teacher}/>
        <Route path="/contact" component={Contact}/>
        <Footer />
    </Router>
</main>