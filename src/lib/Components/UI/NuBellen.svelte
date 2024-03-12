<script>
    import image10 from "$lib/assets/10.jpg"
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
    max-height: 100%;
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
    max-height: 4.5rem;
    
    
    
  }
  
  p{
    font-family: 'Montserrat';
    line-height: 1; 
    width: auto;
    height: auto;
    padding: auto;
    font-size: large;
    font-weight:bolder;
    margin: 1rem;
    color: #ffffff;
    text-shadow: 1px 2px 5px #000000;
    
  
    
    
    
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
    color: #f3f0f0;
  }
  .xdd:hover {
    background-color: #627d9a; /* A darker blue */
  }
  #uniqueID a{
    color: black;
  }
  </style>
  
  
  <div>
  
    <div class="card">
        <img src="{image10}" alt="">
    </div>
    <div class ="text">
        <p><a href="tel:32477291260">Tel: 0477-29-12-60</a></p>
        <p>Btw: BE 0859 090 792</p>
        <p><a href = "mailto:Deejay.serge@hotmail.com">Email: Deejay.serge@hotmail.com</a></p>
        
      </div>
      
      <div class='xd'>
        <button id= "uniqueID" class='xdd'><a href="tel:+0477291260">Nu bellen</a></button>
      </div>
  
      
  
  </div>