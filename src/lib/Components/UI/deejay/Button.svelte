<script>
  export let type = "button";
  export let href = null;
  export let mode = null;
  export let color = null;


  const colorPalette = {
  darkestTeal: '#006d6d',
  mediumTeal: '#1d9a9a',
  lightTeal: '#3ac1c1',
  lightestTeal: '#54d8d8',
  brightestTeal: '#88efef'
};
  
</script>

<style>
  button,
  a {
    font: inherit;
    border: 1px solid #fbfbfb;
    background: #E1771E;
    padding: 0.5rem 1rem;
    color: white;
    border-radius: 5px;
    box-shadow: 1px 1px 3px rgba(0, 0, 0, 0.26);
    cursor: pointer;
    text-decoration: none;
    
  }

  button:focus {
    outline: none;
  }

  button:hover,
  button:active,
  a:hover,
  a:active {
    background:#E1771E;
    border-color: #E1771E;
    box-shadow: 1px 1px 8px rgba(77, 51, 51, 0.26);
    
  }

  button:disabled,
  button:disabled:hover,
  button:disabled:active {
    background: #ccc;
    border-color: #ccc;
    color: #959595;
    box-shadow: none;
    cursor: not-allowed;
  }

  .success {
    background: #01a129;
    border-color: #01a129;
  }

  .success:hover,
  .success:active {
    background: #1ac745;
    border-color: #1ac745;
  }

  .outline {
    background: transparent;
    color: #E1771E;
    box-shadow: none;
  }

  .outline:hover,
  .outline:active {
    background: #ffc7de;
    box-shadow: none;
  }

  .outline:disabled,
  .outline:disabled:hover,
  .outline:disabled:active {
    background: transparent;
    color: #ccc;
  }

  .outline.success {
    border-color: #01a129;
    color: #01a129;
  }

  .outline.success:hover,
  .outline.success:active {
    background: #c2ffd1;
  }
  
</style>

{#if href}
  <a {href}>
    <slot />
  </a>
{:else}
  <button class="{mode}  {color}" {type} on:click >
    <slot />
  </button>
{/if}
