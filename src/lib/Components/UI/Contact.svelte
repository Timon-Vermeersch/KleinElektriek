<script>
    import Icon from "$lib/assets/SimpleLineIconsEnvelope.svg"
  import Fb from "../fb.svelte";
    import {createEventDispatcher} from 'svelte'
    const dispatch = createEventDispatcher()
</script>

<style>
 a{
    color: rgb(255, 255, 255);
    padding: 10px 20px; 
    font-size: 16px;
    text-shadow: 2px 0px 4px #000000;
    
    cursor: pointer;
    
  
 }
 a:hover{
   text-decoration: underline;
   
 }


  </style>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<!-- svelte-ignore a11y-no-static-element-interactions -->
<!-- svelte-ignore a11y-missing-attribute -->

<a on:click = {() => {dispatch('changeSite' , 'home')}}>
         Home
</a>

