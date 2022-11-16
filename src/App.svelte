<script lang="ts">
  let count: number = 0;
</script>

<main class="flex h-screen w-screen items-center justify-center flex-col">
  <span class="mb-5 font-bold text-xl"> Svelte + Vite + Tailwind </span>
  <button
    on:click={() => count++}
    class="border border-orange-900 py-2 px-6 bg-orange-500 text-white"
  >
    Click me {count}
  </button>
</main>
