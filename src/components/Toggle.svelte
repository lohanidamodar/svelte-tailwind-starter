<script>
  export let value;
  export let label = "";
</script>

<style lang="postcss">
  label {
    @apply flex items-center cursor-pointer;
  }

  .toggle__dot {
    top: -0.25rem;
    left: -0.25rem;
    transition: all 0.3s ease-in-out;
  }

  input:checked ~ .toggle__dot {
    transform: translateX(100%);
  }
</style>

<div class="flex items-center justify-center w-full mb-24">

  <!-- Toggle Button -->
  <label for="toogleA" class="">
    <!-- toggle -->
    <div class="relative">
      <!-- input -->
      <input
        bind:checked="{value}"
        id="toogleA"
        type="checkbox"
        class="hidden" />
      <!-- line -->
      <div
        class=" toggle__line w-10 h-4 bg-gray-400 rounded-full shadow-inner"></div>
      <!-- dot -->
      <div
        class="{value ? 'bg-pink-500':''} toggle__dot absolute w-6 h-6 bg-white rounded-full shadow
        inset-y-0 left-0"></div>
    </div>
    <!-- label -->
    <div class="ml-3 dark:text-gray-200 text-gray-700 font-medium">{label}</div>
  </label>

</div>
