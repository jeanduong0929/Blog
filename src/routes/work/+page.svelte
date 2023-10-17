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
  <div class="flex flex-col justify-center max-w-screen-lg w-11/12 mx-auto">
    <div in:fly={{ y: 100, duration: 500 }}>
      <h1 class="font-bold text-5xl mt-20">Work Experience.</h1>
      <div class="flex flex-col mt-5">
        <h2 class="font-bold text-lg">Senior Full Stack Developer Trainer</h2>
        <h2 class="text-lg"><strong>Company: </strong>Revature</h2>
        <h2 class="text-lg"><strong>Duration: </strong>2 years to date</h2>
        <h2 class="text-lg">
          <strong>Technologies Used: </strong>Java, Spring, AWS, Postgres,
          Angular, React
        </h2>
      </div>
    </div>

    <div in:fly={{ y: 150, duration: 700 }}>
      <h1 class="font-bold text-4xl mt-20">Description.</h1>
      <p class="mt-2">
        As a senior trainer at Revature, I've had the privilege of guiding
        non-technical associates on their journey into the tech world. My
        primary role involves transforming individuals with no prior coding
        experience into competent full-stack developers within a short span of
        12 weeks. This accelerated learning curve not only stands testimony to
        the dedication of the associates but also to the structured and
        intensive training methods I employ.
      </p>
      <br />
      <p>
        One of the hallmarks of my training stint at Revature has been a
        remarkably low turnover rate. It speaks volumes about the effectiveness
        of the training, the quality of the curriculum, and the overall positive
        environment cultivated for learners.
      </p>
    </div>
  </div>
{:else}
  <Loader />
{/if}
