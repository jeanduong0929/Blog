<script>
  import Loader from "./Loader.svelte";
  import GithubIcon from "$lib/svgs/GithubIcon.svelte";
  import { darkMode } from "$lib/store/darkmode";
  import { pathname } from "$lib/store/pathname";
  import { onMount } from "svelte";
  import { CommandIcon, MoonIcon, SunIcon } from "lucide-svelte";

  let pathnameLoading = true;

  function darkModeToggle() {
    $darkMode = !$darkMode;
    if ($darkMode) {
      localStorage.setItem("darkMode", "true");
    } else {
      localStorage.removeItem("darkMode");
    }
  }

  onMount(() => {
    $pathname = window.location.pathname;
    pathnameLoading = false;
  });
</script>

{#if pathnameLoading}
  <Loader />
{:else}
  <nav
    class="flex items-center justify-between max-w-screen-lg w-11/12 mx-auto py-5"
  >
    <ul class="flex items-center gap-5">
      <li>
        <a
          href="/"
          class="flex items-center gap-3"
          on:click={() => ($pathname = "")}
        >
          <CommandIcon size={24} />
          <h1 class="font-bold text-xl">Bao Duong</h1>
        </a>
      </li>
      <li>
        <a
          href="/about"
          class={`p-2 hover:underline underline-offset-4 ${
            $pathname === "/about" && "bg-[#88ccca] text-white"
          }`}
          on:click={() => ($pathname = "/about")}>About</a
        >
      </li>
      <li>
        <a
          href="/skills"
          class={`p-2 hover:underline underline-offset-4 ${
            $pathname === "/skills" && "bg-[#88ccca] text-white"
          }`}
          on:click={() => ($pathname = "/skills")}>Skills</a
        >
      </li>
      <li>
        <a
          href="/work"
          class={`p-2 hover:underline underline-offset-4 ${
            $pathname === "/work" && "bg-[#88ccca] text-white"
          }`}
          on:click={() => ($pathname = "/work")}>Work</a
        >
      </li>
      <a href="https://github.com/jeanduong0929/blog.git">
        <GithubIcon class="w-6 h-6" />
      </a>
    </ul>

    <ul class="flex items-center gap-5">
      <button type="button" class="cursor-pointer" on:click={darkModeToggle}>
        {#if $darkMode}
          <div class="fade-in p-2 bg-yellow-500 rounded-md">
            <SunIcon size={24} />
          </div>
        {:else}
          <div class="fade-in p-2 bg-purple-500 rounded-md">
            <MoonIcon size={24} />
          </div>
        {/if}
      </button>
    </ul>
  </nav>
{/if}
