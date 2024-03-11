<script>
  import image6 from "$lib/assets/7.jpg"
  import Button from "./Button.svelte";
    

  const colorPalette = {
  darkestTeal: '#006d6d',
  mediumTeal: '#1d9a9a',
  lightTeal: '#3ac1c1',
  lightestTeal: '#54d8d8',
  brightestTeal: '#88efef'
};
  
</script>
<style>
  div{
    /* From https://css.glass */

    
    width:500px;
    height:auto;
    display: flex;
    justify-content: space-between;
    flex-direction: column; 
    overflow: hidden;
    align-items: center;
    object-fit: contain;
  }

.card{
  padding: 1rem;
  max-width: 95%;
  max-height: 95%;
  object-fit: cover;
  overflow: auto;
  
  
}

img{
  object-fit: cover;
  width: 100%;
  height: 100%;
  overflow: hidden;
  border-radius: 12px;
}
.text{
  background-color:#2192905b;
  padding: auto;
  padding-bottom: 5rem;
  
}

p{
  font-family: 'Montserrat';
  line-height: 1.6; 
  width: auto;
  height: auto;
  padding: auto;
  font-size: large;
  font-weight:950;
  margin: 1rem;
  color: #000000;
  
  
  
}
.xd{
  height: 5rem;
  background-color:#21929061; 
  padding: auto;
  
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
  
}

.xdd {
  
  background-color:#fca43a; /* Bootstrap primary blue */
  color: #0A0A0ADE;
  padding: 10px 20px;
  
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}
a{
  color: #23198e;
}
.xdd:hover {
  background-color: #627d9a; /* A darker blue */
}
</style>


<div>

  <div class="card">
      <img src="{image6}" alt="">
  </div>
  <div class ="text">
      <p>Komt uw elektricien niet langs voor kleine werkjes? Neem gerust <u><a href="https://www.w3schools.com">contact</a></u> op met mij om een stopcontact of luchter te laten plaatsen, uw nieuwe poolhouse van elektriciteit te laten voorzien, ... en ondertussen hang ik snel uw nieuw kadertje op. </p>
      
    </div>
    
    <div class='xd'>
      <button class='xdd'>Nu bellen</button>
    </div>

  

</div>