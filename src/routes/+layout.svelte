<script>
  import "../app.css";
  import Footer from "$lib/components/Footer.svelte";
  import Navbar from "$lib/components/Navbar.svelte";
  import { darkMode } from "$lib/store/darkmode";
  import { onMount } from "svelte";

  onMount(() => {
    if (localStorage.getItem("darkMode")) {
      $darkMode = true;
    } else {
      $darkMode = false;
    }
  });
</script>

<div
  class={`flex flex-col min-h-screen ${
    $darkMode ? "bg-[#f0e7db] text-[#202023]" : "bg-[#202023] text-[#f0e7db]"
  }`}
>
  <header>
    <Navbar />
  </header>

  <main class="flex-grow">
    <slot />
  </main>

  <footer>
    <Footer />
  </footer>
</div>
