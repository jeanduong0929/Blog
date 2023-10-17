<script>
  import Loader from "$lib/components/Loader.svelte";
  import AngularIcon from "$lib/svgs/AngularIcon.svelte";
  import AwsIcon from "$lib/svgs/AwsIcon.svelte";
  import DatabaseIcon from "$lib/svgs/DatabaseIcon.svelte";
  import JavaIcon from "$lib/svgs/JavaIcon.svelte";
  import NextIcon from "$lib/svgs/NextIcon.svelte";
  import ReactIcon from "$lib/svgs/ReactIcon.svelte";
  import RestIcon from "$lib/svgs/RestIcon.svelte";
  import SpringIcon from "$lib/svgs/SpringIcon.svelte";
  import SvelteIcon from "$lib/svgs/SvelteIcon.svelte";
  import { onMount } from "svelte";
  import { fly } from "svelte/transition";

  let showContent = false;

  onMount(() => {
    showContent = true;
  });
</script>

{#if showContent}
  <div
    class="flex flex-col items-center justify-center max-w-screen-lg w-11/12 mx-auto h-[80vh] gap-14"
  >
    <h1 class="font-bold text-5xl" in:fly={{ y: 100, duration: 500 }}>
      Skills.
    </h1>

    <div class="grid grid-cols-3 gap-5">
      <div
        class="flex flex-col items-start p-5 gap-5"
        in:fly={{ y: 150, duration: 700 }}
      >
        <NextIcon class="h-14 w-14" />
        <h1 class="font-bold text-xl">Next.js 13</h1>
        <p>
          Enables efficient server-side rendering for better performance and SEO
          in web applications.
        </p>
      </div>

      <div
        class="flex flex-col items-start p-5 gap-5"
        in:fly={{ y: 150, duration: 700 }}
      >
        <AngularIcon class="h-14 w-14" />
        <h1 class="font-bold text-xl">Angular</h1>
        <p>
          A comprehensive framework for building dynamic, large-scale
          single-page web applications.
        </p>
      </div>

      <div
        class="flex flex-col items-start p-5 gap-5"
        in:fly={{ y: 150, duration: 700 }}
      >
        <ReactIcon class="h-14 w-14" />
        <h1 class="font-bold text-xl">React</h1>
        <p>
          A library for constructing interactive UIs efficiently and with a
          component-driven architecture.
        </p>
      </div>

      <div
        class="flex flex-col items-start p-5 gap-5"
        in:fly={{ y: 200, duration: 900 }}
      >
        <JavaIcon class="h-14 w-14" />
        <h1 class="font-bold text-xl">Java</h1>
        <p>
          A platform-independent language central to enterprise applications and
          system development.
        </p>
      </div>

      <div
        class="flex flex-col items-start p-5 gap-5"
        in:fly={{ y: 200, duration: 900 }}
      >
        <SpringIcon class="h-14 w-14" />
        <h1 class="font-bold text-xl">Spring</h1>
        <p>
          Offers a robust framework for building scalable and secure Java
          applications with ease.
        </p>
      </div>

      <div
        class="flex flex-col items-start p-5 gap-5"
        in:fly={{ y: 200, duration: 900 }}
      >
        <DatabaseIcon class="h-14 w-14" />
        <h1 class="font-bold text-xl">SQL</h1>
        <p>
          The cornerstone for relational database management, essential for data
          storage and retrieval.
        </p>
      </div>

      <div
        class="flex flex-col items-start p-5 gap-5"
        in:fly={{ y: 250, duration: 1100 }}
      >
        <SvelteIcon class="h-14 w-14" />
        <h1 class="font-bold text-xl">Svelte</h1>
        <p>
          An innovative compiler-based approach to building fast and lean web
          applications.
        </p>
      </div>

      <div
        class="flex flex-col items-start p-5 gap-5"
        in:fly={{ y: 250, duration: 1100 }}
      >
        <AwsIcon class="h-14 w-14" />
        <h1 class="font-bold text-xl">AWS</h1>
        <p>
          A leading cloud service provider that offers a vast array of
          infrastructure and computing resources.
        </p>
      </div>

      <div
        class="flex flex-col items-start p-5 gap-5"
        in:fly={{ y: 250, duration: 1100 }}
      >
        <RestIcon class="h-14 w-14" />
        <h1 class="font-bold text-xl">REST</h1>
        <p>
          A standard architecture for designing networked applications,
          simplifying communication between client and server through stateless
          interactions.
        </p>
      </div>
    </div>
  </div>
{:else}
  <Loader />
{/if}
