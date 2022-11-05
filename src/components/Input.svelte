<script lang="ts">
  export let id: string;
  export let type: string = "email";
  export let label: string;
  export let value: string;
  export let placeholder: string = "";
  export let required: boolean = false;
  export let rounded: boolean = false;
  export let circled: boolean = false;
  const typeAction = (node) => {
    node.type = type;
  };
</script>

<div class="bg-white">
  {#if label?.length > 0}
    <div class="flex">
      <label
        for=""
        class="text-gray-500 text-xs top-2 left-5 px-1 text-left  relative bg-white"
      >
        {label}
      </label>
    </div>
  {/if}

  <input
    {id}
    on:change
    use:typeAction
    bind:value
    {required}
    {placeholder}
    class:rounded
    class:rounded-full={circled}
    class="border-2  w-full focus:outline-none text-gray-700 py-2 px-5"
  />
</div>
