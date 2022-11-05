<script lang="ts">
  import { Button, Input } from "./components/index";
  let colors = [
    "blue",
    "dark",
    "light",
    "green",
    "red",
    "yellow",
    "purple",
    "orange",
    "cyan",
    "pink",
  ];
  let value = "";
  $: console.log(value);
</script>

<!--main>
  <p class="text-teal-500">Tailwind is working</p>
  <div>
    {#each colors as color}
      <Button {color}>Merhaba</Button>
    {/each}
  </div>
  <hr style="width:100%;border:1px solid red" />
  <div>
    {#each colors as color}
      <Button gradient {color}>Merhaba</Button>
    {/each}
  </div>
  <hr style="width:100%;border:1px solid red" />

  <div>
    {#each colors as color}
      <Button shadow {color}>Merhaba</Button>
    {/each}
  </div>
</main-->
<form action="">
  <Input
    id="qwe"
    bind:value
    label="deneme"
    required
    placeholder="placeholder test"
  />
  <Input
    id="qwe"
    bind:value
    label="deneme"
    required
    circled
    placeholder="placeholder test"
  />
  <button>qwe</button>
</form>
