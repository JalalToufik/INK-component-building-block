<script>
    import '../lib/style/fonts.css'
    import Header from "../lib/header/Header.svelte"
</script>

<Header />

<main>
  <slot />
</main>

<style>

  :global(*){
    box-sizing: border-box;
    text-decoration: none;
    list-style: none;
    margin: 0;
    padding: 0;
    font-family: var(--copy-font);
  }

  /* Color variable */

  :global(:root){
    --charcoal: #051A1A;
    --candelLight: #FFDA1D;
    --justWhite: #FFFFFF;
    --jungleDarkGreen: #0c2121;
    --jungleGreen: #163A3A;
    --plantGreen: #179446;
    --pictonBlue: #3DBAE1;
    --copy-font: 'Apercu pro', sans-serif;
    --paragraph-font: 'Jubilat', serif;
    --header-font: 'Kirang Haerang', sans-serif;
    --link-hover-color: #FFDA1D;
    --button-hover-color: #FFFFFF;
    --top-nav-sponsor-button-hover-color: #051A1A;
  }


:global(body) {
  background-color: var(--jungleDarkGreen);
  color: var(--justWhite);
  width: 100%;
  height: 100vh;
  overflow-x: hidden;
  display: flex;
  flex-direction: column;
  overflow: hidden;

  overflow-y: scroll; 
  overflow-x: scroll;
}

:global(main){
  margin-top: 6em;
}

:global(h1,h2){
  font-family: 'Kirang Haerang';
}
  
</style>