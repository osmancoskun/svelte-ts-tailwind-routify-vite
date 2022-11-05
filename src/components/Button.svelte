<script lang="ts">
  export let type: string = "button";
  export let color: string = "blue";
  export let rounded: boolean = false;
  export let shadow: boolean = false;
  export let gradient: string | boolean = false;
  let colors = {
    blue: {
      default: `
      text-white bg-blue-500 hover:bg-blue-800 
      `,
      gradient: `
      text-white 
      bg-gradient-to-r from-blue-500 via-blue-600 to-blue-700 
      hover:ring-2 hover:ring-blue-700
      `,
      shadow: "shadow-blue-500/50 shadow-xl",
    },

    dark: {
      default: `
      text-white bg-gray-800 hover:bg-gray-500 
      `,
      gradient: `
      text-white 
      bg-gradient-to-r from-zinc-300 via-zinc-500 to-zinc-700 
      hover:ring-2 hover:ring-zinc-700
      `,
      shadow: "shadow-zinc-500/50 shadow-xl",
    },
    light: {
      default: `
      text-black hover:text-white bg-gray-200 hover:bg-gray-500 
        `,
      gradient: `
      text-black 
      bg-gradient-to-r from-zinc-100 via-zinc-300 to-zinc-500 
      hover:ring-2 hover:ring-zinc-700
      `,
      shadow: "shadow-zinc-500/50 shadow-xl",
    },
    green: {
      default: `
      text-white bg-green-500 hover:bg-green-700
      `,
      gradient: `
      text-white 
      bg-gradient-to-r from-green-500 via-green-600 to-green-700 
      hover:ring-2 hover:ring-green-700
      `,
      shadow: "shadow-green-500/50 shadow-xl",
    },
    red: {
      default: `
       text-white bg-red-500 hover:bg-red-700
        `,
      gradient: `
      text-white 
      bg-gradient-to-r from-red-500 via-red-550 to-red-700 
      hover:ring-2 hover:ring-red-700
      `,
      shadow: "shadow-red-500/50 shadow-xl",
    },
    yellow: {
      default: `
      text-white bg-yellow-400 hover:bg-yellow-500 
      `,
      gradient: `
      text-white 
      bg-gradient-to-r from-yellow-400 via-yellow-550 to-yellow-700 
      hover:ring-2 hover:ring-yellow-700
      `,
      shadow: "shadow-yellow-500/50 shadow-xl",
    },
    purple: {
      default: `
      text-white bg-purple-400 hover:bg-purple-700
      `,
      gradient: `
      text-white 
      bg-gradient-to-r from-purple-400 via-purple-550 to-purple-700 
      hover:ring-2 hover:ring-purple-700
      `,
      shadow: "shadow-purple-500/50 shadow-xl",
    },
    orange: {
      default: `
      text-white bg-orange-500 hover:bg-orange-700  
      `,
      gradient: `
      text-white
      bg-gradient-to-r from-orange-500 via-orange-600 to-orange-700 
      hover:ring-2 hover:ring-orange-700
      `,
      shadow: "shadow-orange-500/50 shadow-xl",
    },
    cyan: {
      default: `
      text-white bg-cyan-400 hover:bg-cyan-700
      `,
      gradient: `
      text-white 
      bg-gradient-to-r from-cyan-400 via-cyan-550 to-cyan-700 
      hover:ring-2 hover:ring-cyan-600
      `,
      shadow: "shadow-cyan-500/50 shadow-xl",
    },
    pink: {
      default: `
      text-white bg-pink-400 hover:bg-pink-700
      `,
      gradient: `
      text-white 
      bg-gradient-to-r from-pink-400 via-pink-600 to-pink-700 
      hover:ring-2 hover:ring-red-800
      `,
      shadow: " shadow-pink-500/50 shadow-xl ",
    },
  };
</script>

<button
  on:click
  on:dblclick
  {type}
  class={`
    px-5 py-2.5 mx-2 my-1
    text-sm
    border-none
    focus:border-none
    focus:outline-none
    ${shadow ? colors[color].shadow : ""}
    ${gradient ? colors[color].gradient : colors[color].default}
    `}
  class:rounded-full={rounded}
>
  <slot />
</button>
