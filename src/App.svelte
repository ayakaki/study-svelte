<script>
  import { Router, Link, Route } from 'svelte-routing';
  import About from './pages/About.svelte';
</script>

<Router>
  <nav>
    <ul>
      <li><Link to="">home</Link></li>
      <li><Link to="about">about</Link></li>
    </ul>
  </nav>
  <main>
    <Route path="">
      <h1>Home</h1>
    </Route>
    <Route path="about">
      <About />
    </Route>
  </main>
</Router>
