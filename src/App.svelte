<script>
  import Toggle from "./components/Toggle.svelte";
  let darkMode = true;
</script>

<style>

</style>

<main class="{darkMode ? 'dark' : ''}">
  <div class="w-full bg-pink-200 dark:bg-gray-800">
    <div class="container mx-auto text-center py-4">
      <h1 class="font-bold text-2xl dark:text-white">Hello World!</h1>
      <span class="dark:text-white"> Welcome to Svelte-Tailwind starter.</span>
      <div class="my-4">
        <a
          target="_blank"
          class="p-2 bg-pink-600 hover:bg-pink-500 rounded text-white m-2"
          href="https://github.com/lohanidamodar/svelte-tailwind-starter">
          Star Github
        </a>
      </div>
      <Toggle label="Dark Mode" bind:value="{darkMode}" />
    </div>
  </div>
</main>
