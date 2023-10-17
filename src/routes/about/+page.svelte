<script>
  import Loader from "$lib/components/Loader.svelte";
  import { onMount } from "svelte";
  import { fly } from "svelte/transition";

  let showContent = false;

  onMount(() => {
    showContent = true;
  });
</script>

{#if showContent}
  <div
    class="flex flex-col justify-center h-[70vh] max-w-screen-lg w-11/12 mx-auto gap-10"
  >
    <div class="flex justify-between gap-10 w-full">
      <div
        class="flex flex-col items-start gap-5 w-1/2"
        in:fly={{ y: 100, duration: 500 }}
      >
        <h1 class="font-bold text-5xl">About.</h1>
        <p>
          Hello! I'm Bao Duong. Originally hailing from Vietnam, my journey led
          me to Denver, Colorado, when I was just six years old. Today, I call
          the vibrant city of Tampa, Florida, my home.
        </p>
      </div>

      <div class="w-1/2" />
    </div>

    <div class="flex justify-between gap-10 w-full">
      <div class="w-1/2" />
      <div
        class="flex flex-col items-start gap-5 w-1/2"
        in:fly={{ y: 150, duration: 700 }}
      >
        <h1 class="font-bold text-5xl">Education.</h1>
        <p>
          Education has always been a pivotal part of my journey. I'm proud to
          say that I hold a bachelor's degree in Computer Science from the
          prestigious Colorado School of Mines.
        </p>
      </div>
    </div>

    <div class="flex justify-between gap-10 w-full">
      <div
        class="flex flex-col items-start gap-5 w-1/2"
        in:fly={{ y: 200, duration: 900 }}
      >
        <h1 class="font-bold text-5xl">Philosophy.</h1>
        <p>
          One of my core beliefs is that "smarts will get you far, but hard work
          and discipline will get you farther." This philosophy has been the
          driving force behind every line of code I write, every problem I
          solve, and every challenge I tackle.
        </p>
      </div>
      <div class="w-1/2" />
    </div>

    <div class="flex justify-between gap-10 w-full">
      <div class="w-1/2" />
      <div
        class="flex flex-col items-start gap-5 w-1/2"
        in:fly={{ y: 250, duration: 1100 }}
      >
        <h1 class="font-bold text-5xl">Hobbies.</h1>
        <p>
          Outside of the digital realm, I have a passion for powerlifting. The
          discipline and determination I exhibit in this sport are the very
          qualities I bring into my professional life.
        </p>
      </div>
    </div>
  </div>
{:else}
  <Loader />
{/if}
