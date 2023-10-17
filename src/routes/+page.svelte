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
    class="flex flex-col items-center justify-center max-w-screen-lg w-11/12 mx-auto h-[70vh]"
    in:fly={{ y: 100, duration: 500 }}
  >
    <h1 class="font-bold text-5xl">Portfolio.</h1>
  </div>
{:else}
  <Loader />
{/if}
