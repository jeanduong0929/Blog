<script>
  import { Loader2 } from "lucide-svelte";
</script>

<div
  class="fixed flex items-center justify-center inset-0 backdrop-blur-md fade-in z-30"
>
  <Loader2 class="animate-spin" size={50} />
</div>

<style>
  .fade-in {
    animation: fadeIn 0.5s ease-in-out;
  }

  @keyframes fadeIn {
    0% {
      opacity: 0;
    }

    100% {
      opacity: 1;
    }
  }
</style>
